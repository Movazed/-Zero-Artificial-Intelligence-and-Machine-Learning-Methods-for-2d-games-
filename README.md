# Alpha-Zero-Artificial-Intelligence-and-Machine-Learning-Methods-for-2d-games-
AlphaZero is a computer program developed by artificial intelligence research company DeepMind to master the games of chess, shogi and go. This algorithm uses an approach similar to AlphaGo Zero.
AlphaZeroFromScratch
Out of the box implementation based on the code of the tutorial: AlphaZero


Some Helpful Resources

AlphaZero-Paper: https://arxiv.org/pdf/1712.01815.pdf

Paper-Walkthrough: https://youtu.be/0slFo1rV0EM

MCTS-Explained: https://youtu.be/UXW2yZndl7U

AlphaZero-Explained: https://youtu.be/62nq4Zsn8vc


AlphaZero is a computer program developed by artificial intelligence research company DeepMind to master the games of chess, shogi and go. This algorithm uses an approach similar to AlphaGo Zero.

On December 5, 2017, the DeepMind team released a preprint paper introducing AlphaZero, which within 24 hours of training achieved a superhuman level of play in these three games by defeating world-champion programs Stockfish, Elmo, and the three-day version of AlphaGo Zero. In each case it made use of custom tensor processing units (TPUs) that the Google programs were optimized to use.[1] AlphaZero was trained solely via self-play using 5,000 first-generation TPUs to generate the games and 64 second-generation TPUs to train the neural networks, all in parallel, with no access to opening books or endgame tables. After four hours of training, DeepMind estimated AlphaZero was playing chess at a higher Elo rating than Stockfish 8; after nine hours of training, the algorithm defeated Stockfish 8 in a time-controlled 100-game tournament (28 wins, 0 losses, and 72 draws). The trained algorithm played on a single machine with four TPUs.

DeepMind's paper on AlphaZero was published in the journal Science on 7 December 2018; however, the AlphaZero program itself has not been made available to the public.[5] In 2019, DeepMind published a new paper detailing MuZero, a new algorithm able to generalise AlphaZero's work, playing both Atari and board games without knowledge of the rules or representations of the game.

Relation to AlphaGo Zero
Further information: AlphaGo Zero
AlphaZero (AZ) is a more generalized variant of the AlphaGo Zero (AGZ) algorithm, and is able to play shogi and chess as well as Go. Differences between AZ and AGZ include:[1]

AZ has hard-coded rules for setting search hyperparameters.
The neural network is now updated continually.
AZ doesn't use symmetries, unlike AGZ.
Chess can end in a draw unlike Go; therefore, AlphaZero takes into account the possibility of a drawn game.
Stockfish and Elmo
Further information: Stockfish (chess) and elmo (shogi engine)
Comparing Monte Carlo tree search searches, AlphaZero searches just 80,000 positions per second in chess and 40,000 in shogi, compared to 70 million for Stockfish and 35 million for Elmo. AlphaZero compensates for the lower number of evaluations by using its deep neural network to focus much more selectively on the most promising variation.[1]

Training
AlphaZero was trained solely via self-play, using 5,000 first-generation TPUs to generate the games and 64 second-generation TPUs to train the neural networks. In parallel, the in-training AlphaZero was periodically matched against its benchmark (Stockfish, Elmo, or AlphaGo Zero) in brief one-second-per-move games to determine how well the training was progressing. DeepMind judged that AlphaZero's performance exceeded the benchmark after around four hours of training for Stockfish, two hours for Elmo, and eight hours for AlphaGo Zero.[1]

Preliminary results
Outcome
Chess
In AlphaZero's chess match against Stockfish 8 (2016 TCEC world champion), each program was given one minute per move. AlphaZero was flying the English flag, while Stockfish the Norwegian. Stockfish was allocated 64 threads and a hash size of 1 GB, a setting that Stockfish's Tord Romstad later criticized as suboptimal. AlphaZero was trained on chess for a total of nine hours before the match. During the match, AlphaZero ran on a single machine with four application-specific TPUs. In 100 games from the normal starting position, AlphaZero won 25 games as White, won 3 as Black, and drew the remaining 72. In a series of twelve, 100-game matches (of unspecified time or resource constraints) against Stockfish starting from the 12 most popular human openings, AlphaZero won 290, drew 886 and lost 24.

Shogi
AlphaZero was trained on shogi for a total of two hours before the tournament. In 100 shogi games against Elmo (World Computer Shogi Championship 27 summer 2017 tournament version with YaneuraOu 4.73 search), AlphaZero won 90 times, lost 8 times and drew twice. As in the chess games, each program got one minute per move, and Elmo was given 64 threads and a hash size of 1 GB.

Go
After 34 hours of self-learning of Go and against AlphaGo Zero, AlphaZero won 60 games and lost 40.

Analysis
DeepMind stated in its preprint, "The game of chess represented the pinnacle of AI research over several decades. State-of-the-art programs are based on powerful engines that search many millions of positions, leveraging handcrafted domain expertise and sophisticated domain adaptations. AlphaZero is a generic reinforcement learning algorithm – originally devised for the game of go – that achieved superior results within a few hours, searching a thousand times fewer positions, given no domain knowledge except the rules."[1] DeepMind's Demis Hassabis, a chess player himself, called AlphaZero's play style "alien": It sometimes wins by offering counterintuitive sacrifices, like offering up a queen and bishop to exploit a positional advantage. "It's like chess from another dimension."

Given the difficulty in chess of forcing a win against a strong opponent, the +28 –0 =72 result is a significant margin of victory. However, some grandmasters, such as Hikaru Nakamura and Komodo developer Larry Kaufman, downplayed AlphaZero's victory, arguing that the match would have been closer if the programs had access to an opening database (since Stockfish was optimized for that scenario). Romstad additionally pointed out that Stockfish is not optimized for rigidly fixed-time moves and the version used was a year old.

Similarly, some shogi observers argued that the Elmo hash size was too low, that the resignation settings and the "EnteringKingRule" settings (cf. shogi § Entering King) may have been inappropriate, and that Elmo is already obsolete compared with newer programs.

Reaction and criticism
Papers headlined that the chess training took only four hours: "It was managed in little more than the time between breakfast and lunch."[2][15] Wired described AlphaZero as "the first multi-skilled AI board-game champ". AI expert Joanna Bryson noted that Google's "knack for good publicity" was putting it in a strong position against challengers. "It's not only about hiring the best programmers. It's also very political, as it helps make Google as strong as possible when negotiating with governments and regulators looking at the AI sector."

Human chess grandmasters generally expressed excitement about AlphaZero. Danish grandmaster Peter Heine Nielsen likened AlphaZero's play to that of a superior alien species.[9] Norwegian grandmaster Jon Ludvig Hammer characterized AlphaZero's play as "insane attacking chess" with profound positional understanding.[2] Former champion Garry Kasparov said, "It's a remarkable achievement, even if we should have expected it after AlphaGo."

Grandmaster Hikaru Nakamura was less impressed, stating: "I don't necessarily put a lot of credibility in the results simply because my understanding is that AlphaZero is basically using the Google supercomputer and Stockfish doesn't run on that hardware; Stockfish was basically running on what would be my laptop. If you wanna have a match that's comparable you have to have Stockfish running on a supercomputer as well."

Top US correspondence chess player Wolff Morrow was also unimpressed, claiming that AlphaZero would probably not make the semifinals of a fair competition such as TCEC where all engines play on equal hardware. Morrow further stated that although he might not be able to beat AlphaZero if AlphaZero played drawish openings such as the Petroff Defence, AlphaZero would not be able to beat him in a correspondence chess game either.[18]

Motohiro Isozaki, the author of YaneuraOu, noted that although AlphaZero did comprehensively beat Elmo, the rating of AlphaZero in shogi stopped growing at a point which is at most 100–200 higher than Elmo. This gap is not that high, and Elmo and other shogi software should be able to catch up in 1–2 years.[19]

Final results
DeepMind addressed many of the criticisms in their final version of the paper, published in December 2018 in Science.[4] They further clarified that AlphaZero was not running on a supercomputer; it was trained using 5,000 tensor processing units (TPUs), but only ran on four TPUs and a 44-core CPU in its matches.[20]

Chess
In the final results, Stockfish version 8 ran under the same conditions as in the TCEC superfinal: 44 CPU cores, Syzygy endgame tablebases, and a 32GB hash size. Instead of a fixed time control of one move per minute, both engines were given 3 hours plus 15 seconds per move to finish the game. In a 1000-game match, AlphaZero won with a score of 155 wins, 6 losses, and 839 draws. DeepMind also played a series of games using the TCEC opening positions; AlphaZero also won convincingly. Stockfish needed 10-to-1 time odds to match AlphaZero.

Shogi
Similar to Stockfish, Elmo ran under the same conditions as in the 2017 CSA championship. The version of Elmo used was WCSC27 in combination with YaneuraOu 2017 Early KPPT 4.79 64AVX2 TOURNAMENT. Elmo operated on the same hardware as Stockfish: 44 CPU cores and a 32GB hash size. AlphaZero won 98.2% of games when playing sente (i.e. having the first move) and 91.2% overall.

Reactions and criticisms
Human grandmasters were generally impressed with AlphaZero's games against Stockfish. Former world champion Garry Kasparov said it was a pleasure to watch AlphaZero play, especially since its style was open and dynamic like his own.

In the computer chess community, Komodo developer Mark Lefler called it a "pretty amazing achievement", but also pointed out that the data was old, since Stockfish had gained a lot of strength since January 2018 (when Stockfish 8 was released). Fellow developer Larry Kaufman said AlphaZero would probably lose a match against the latest version of Stockfish, Stockfish 10, under Top Chess Engine Championship (TCEC) conditions. Kaufman argued that the only advantage of neural network–based engines was that they used a GPU, so if there was no regard for power consumption (e.g. in an equal-hardware contest where both engines had access to the same CPU and GPU) then anything the GPU achieved was "free". Based on this, he stated that the strongest engine was likely to be a hybrid with neural networks and standard alpha–beta search.

AlphaZero inspired the computer chess community to develop Leela Chess Zero, using the same techniques as AlphaZero. Leela contested several championships against Stockfish, where it showed roughly similar strength to Stockfish, although Stockfish has since pulled away.

In 2019 DeepMind published MuZero, a unified system that played excellent chess, shogi, and go, as well as games in the Atari Learning Environment, without being pre-programmed with their rules.
