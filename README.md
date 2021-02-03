# rnn-patterns-data

# Plane wave propagation: 

train.npy: Training data set of wave propagation and is an array of size (240, 200, 64,64), which represents 240 sequences of 200 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame training clips (i.e. frame 1–20, 11–30, etc), each of which represents a training data point.

valid.npy: Validation data set of wave propagation and is an array of size (30, 200, 64,64), which represents 30 sequences of 200 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame clips (i.e. frame 1–20, 11–30, etc) and clips serve as the validation data points. 

test_ground_truth.npy: Ground truth data for predictions. The array is of size (100,200,64,64), which is 100 sequences of 200 frames. Size of each frame is (64,64). 

test_prediction.npy: Array of prediction results of 50 frames given 10 input frames from ground truth data. The ground-truth sequence of 200 frames is divided into staggered 60-frame clips (i.e. frame 1–60, 11–70, etc), each of which is one prediction. There are 15 predictions from one 200-frame sequence. Thus, the array is of size (1500, 60, 64, 64) and has 1500 predictions and each case has 60 frames of size (64,64).  In each 60-frame prediction, frame 1-10 is input and frame 11-60 is output. In this array, frame 1-10 of these 1500 predictions are blank and could be found from the ground truth. 

# Grain growth:

All training and testing data are included in this directory, the details goes as follow:
train_hybrid_thin.npz:includes the training data for the RNN-LSTM model. The size of the npz is (30400, 1, 64, 64), which is consisted of (20, 1, 64, 64) (20 frame) training clips.

valid_hybrid_thin.npz: Includes the validation data set for the RNN-LSTM model. The npz file is consistsd of 380 20-frame validation clips.
test_hybrid_thin_200_frame_200615.npy:Includes the testing data for the RNN-LSTM model. The size of the npy is (1000, 200, 64, 64), which is consisted of 1000 200-frame testing clips.

test_hybrid_thin_200_frame_256_200618.npy:Includes the 256*256 pixel testing data for the RNN-LSTM model. The size is (100, 200, 256, 256), which is consisted of 100 200-frame 256*256 pixel testing clips.

Test_200_frame_200615.zip:Includes 1000 subdirectories listing from 0 to 999, each of the directory contains the ground truth and prediction data for the test cases. Each subdirectory contains 2 nay files: gt_rescaled.npy and pd_rescaled.npy, where gt contains ground truth and pd contains prediction data.

Test_200_frame_256_200624.zip: Inclues 20 subdirectories listing from 0 to 19, each of the directory contains the ground truth and prediction data for the test cases. Each subdirectory contains 2 nay files: gt.npy and pd.npy, where gt contains ground truth and pd contains prediction data.

# Spinodal decomposition:

train.npy: Training data set of spinodal decomposition and is an array of size (640, 100, 64,64), which represents 640 sequences of 100 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame training clips (i.e. frame 1–20, 11–30, etc), each of which represents a training data point.

valid.npy: Validation data set of spinodal decomposition and is an array of size (159, 100, 64,64), which represents 159 sequences of 100 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame clips (i.e. frame 1–20, 11–30, etc) and clips serve as the validation data points. 

test_ground_truth_1_input_frame.npy: Ground truth data for predictions with 1 input frame. The array is of size (510,201,64,64), which is 510 sequences of 201 frames. Size of each frame is (64,64). Frame 1 is used as the input frame. 

test_prediction_1_input_frame.npy: Prediction of 200 frames given 1 frame as input. The array is of size (510,201,64,64), which is 510 sequences of 201 frames. Size of each frame is (64,64). The first frame of each sequence represents input and is set as blank in this array. 

test_ground_truth_artificial_initial_config.npy: Ground truth data for predictions of artificial bi-phasic configurations. The array is of size (15, 201, 64, 64), which is 15 sequences of 201 frames. Frame 1 is the input frame for prediction. 

test_prediction_artificial_initial_coonfig.npy: Prediction of 200 frames of artificial bi-phase configurations. The array is of size (15, 201,64,64), which is 15 cases of 201 frames. The first frame of these 15 sequences are the input frames and are blank in this array. 

test_ground_truth_10_input_frames.npy: Ground truth data for predictions with 10 input frames. The array is of size (510,210,64,64), which is 510 sequences of 210 frames. Size of each frame is (64,64). Frame 1-10 are the input frames. 

test_prediction_10_input_frames.npy: Prediction of 200 frames given 10 frames as input. The array is of size (510,210,64,64), which is 510 sequences of 210 frames. The frame 1-10 of each sequence represent input and are set as blank in this array. 

test_ground_truth_256x256.npy: Ground truth data for predictions with 1 input frame. The array is of size (510,201,256,256), which is 510 sequences of 201 frames. Size of each frame is (256,256). Frame 1 is used as the input frame. 

test_prediction_256x256.npy: Prediction of 200 frames given 1 frame as input. The array is of size (510,201, 256, 256), which is 510 sequences of 201 frames. Size of each frame is (256,256).  The first frame of each sequence represents input and is set as blank in this array. 

# Dendrite growth:

train.npy: Training data set of dendrite growth and is an array of size (940, 100, 64,64), which represents 940 sequences of 100 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame training clips (i.e. frame 1–20, 11–30, etc), each of which represents a training data point.

valid.npy: Validation data set of dendrite growth and is an array of size (60, 100, 64,64), which represents 60 sequences of 100 frames. Size of each frame is (64,64). Each simulation sequence is divided into staggered 20-frame clips (i.e. frame 1–20, 11–30, etc) and clips serve as the validation data points. 

test_ground_truth.npy: Ground truth data for predictions with 10 input frames. The array is of size (100,100,64,64), which is 100 sequences of 100 frames. Size of each frame is (64,64). The first dimension of the array is the number of simulations. 

test_prediction.npy: Array of prediction results of 50 frames given 10 input frames from ground truth data. The ground-truth sequence of 100 frames is divided into staggered 60-frame clips (i.e. frame 1–60, 11–70, etc), each of which is one prediction. There are 5 predictions from one 100-frame sequence. Thus, the array is of size (500, 60, 64, 64). The array has 500 predictions and each case has 60 frames of size (64,64).  In each 60-frame prediction, frame 1-10 is input and frame 11-60 is output. In this array, frame 1-10 of these 500 predictions are blank and could be found from the ground truth.

test_ground_truth_K-0p8-1p2.npy: Ground truth data for predictions with 10 input frames where K values range from (0.8,1.2). The array is of size (10,100,64,64), which is 10 sequences of 100 frames. Size of each frame is (64,64). 

test_prediction_K-0p8-1p2.npy: Array of prediction results of 50 frames given 10 input frames from ground truth data where K values range from (0.8,1.2). The ground-truth sequence of 100 frames is divided into staggered 60-frame clips (i.e. frame 1–60, 11–70, etc), each of which is one prediction. There are 5 predictions from one 100-frame sequence. Thus, the array is of size (50, 60, 64, 64). The array has 50 predictions and each case has 60 frames of size (64,64).  In each 60-frame prediction, frame 1-10 is input and frame 11-60 is output. In this array, frame 1-10 of these 50 predictions are blank and could be found from the ground truth.

test_ground_truth_K-2-2p4.npy: Ground truth data for predictions with 10 input frames where K values range from (2,2.4). The array is of size (10,100,64,64), which is 10 sequences of 100 frames. Size of each frame is (64,64).

test_prediction_K-2-2p4.npy: Array of prediction results of 50 frames given 10 input frames from ground truth data where K values range from (2,2.4). The ground-truth sequence of 100 frames is divided into staggered 60-frame clips (i.e. frame 1–60, 11–70, etc), each of which is one prediction. There are 5 predictions from one 100-frame sequence. Thus, the array is of size (50, 60, 64, 64). The array has 50 predictions and each case has 60 frames of size (64,64).  In each 60-frame prediction, frame 1-10 is input and frame 11-60 is output. In this array, frame 1-10 of these 50 predictions are blank and could be found from the ground truth.
