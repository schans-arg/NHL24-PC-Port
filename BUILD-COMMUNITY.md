Download and extract the complete source ZIP from this project's first Release before using these commands. GitHub's automatic source ZIP is the patch project.

# Build the preview

Base: HajDEO/nhl24pc bef7999707db27884cabe5780f301c4a5d2abdc8.
This archive contains the locally modified source and checked-out submodule files.
The shipped nhl24.exe was built in Release using LLVM-MinGW 20261006 UCRT x86_64
(Clang 23.1.0), CMake 4.4.4 and Ninja. CMake downloads additional pinned dependencies
when required; see CMakeLists.txt and externals/. Internet access is needed for those.

From a Windows shell with LLVM-MinGW/bin, CMake and Ninja on PATH:

    cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=Release -DCMAKE_C_COMPILER=x86_64-w64-mingw32-clang -DCMAKE_CXX_COMPILER=x86_64-w64-mingw32-clang++ -DENABLE_TESTS=OFF -DENABLE_UPDATER=OFF -DENABLE_DISCORD_RPC=OFF
    cmake --build build --target nhl24 --parallel 4
    x86_64-w64-mingw32-clang -O2 -Wall -Wextra -Werror -municode -mwindows -DPORT_NHL24=1 -Wl,--no-insert-timestamp tools/community_entry.c -lcomdlg32 -o "NHL 24.exe"

These are relocation-neutral build directions derived from the local build cache;
an independent clean rebuild has not been performed for this preview. Preserve all
third-party licenses. The original runtime SHA-256 is in RELEASE-RUNTIME.sha256.
No game files are required to compile the runtime. You provide game data at run time.
