# Lời giải "/\*Tờ này để làm nháp\*/ IV"

## A. Đếm tuổi

Ta có phương trình nghiệm nguyên với x là số tuổi của anh Khánh, y là số tuổi của anh Long: (y-5)=(x-5)\*A và y=x\*B. Giải ra ta sẽ được số tuổi anh Khánh. Nhớ xét trường hợp tuổi anh Khánh có thể bị âm.

#### Độ phức tạp : O(1).

## B. Đếm nhiều lần

Khi gặp truy vấn 1, ta sẽ kiểm tra xem nếu ô mình đang xét chưa có bóng thì sẽ thêm bóng vào và dùng cấu trúc dữ liệu DSU để nối các quả bóng trong các ô xung quanh thành một nhóm. Khi gặp truy vấn 2, kiểm tra xem trong ô có bóng không, nếu có thì in ra size của DSU, nếu không thì in ra 0. Có thể sử dụng nén đường để giảm độ phức tạp.

#### Độ phức tạp : O(q).

## C. Đếm ngón tay.

Ta tính tổng số ngón tay của tất cả mọi người trừ anh Long, và đếm số cách giơ ngón tay để tổng số ngón tay chia N dư 1.

#### Độ phức tạp : O(n).

## D. Ngắm sao

### Cách 1 :

Lấy một ngôi sao làm mốc, tính góc tạo bởi đường thằng nối từ nó đến ngôi sao khác vào trục tung của tọa độ bằng hàm atan2(x,y). atan2(x,y) sẽ trả về góc tạo bởi đường thẳng từ điểm (0,0) và điểm (x,y) với trục Ox. Sort lại các ngôi sao theo góc vừa tính. Lấy ngôi sao đầu tiên, và tìm kiếm ngôi sao đầu tiên có số đo góc khác chính nó, ta được 3 ngôi sao có diện tích dương và không có ngôi sao nào nằm chính giữa nó. Hàm atan2(x,y) có thể được thay thế bằng các công thức tính cho đồ thị đường thẳng khác.

#### Độ phức tạp : O(n\*log2(n)).

### Cách 2 :

Lấy 2 ngôi sao bất kì làm mốc, ta tìm ngôi sao gần đường thẳng trên nhất mà không nằm trên đường thẳng. Lấy 3 ngôi sao trên, ta được 3 ngôi sao thỏa mãn đề bài.

#### Độ phức tạp : O(n\*log2(n)).

## E. Ngắm ảnh

Nếu trong 2 số N và M có 1 số chắn thì in ra "YES", nếu không thì xét K, nếu K bằng 1 thì in ra "YES", ngược lại in ra "NO".

*Chứng minh: Ta thấy rằng nếu N hoặc M chẵn thì ta sẽ có cách ghép cặp 2 ô cạnh nhau lại, như vậy ta có một cách đi là đi lại trong 2 cặp cạnh đến lúc nào hết thì chuyển sang cặp cạnh khác. Nếu N và M đều lẻ thì ta chỉ có thể đi được 1 lần mà không đi được thêm lần nào khác do không có tính chất trên.*

#### Độ phức tạp : O(1).

## F. Ngắm mưa sao băng.

Ta dùng phương pháp QHĐ dp[i][j] là đến số thứ i với số thứ i là j. dp[i][j] sẽ cập nhật lên các dp[i+1][j*o] với 1<=o<=(k/j). Dù việc chạy có vẻ rất lớn nhưng nếu j càng to thì o cằng nhỏ, do vậy đảm bảo có thể chạy được.

#### Độ phức tạp : O(n\*k\*log2(k)).

## G. Làm bánh!

Ta sẽ sort lại toàn bộ các số, và ta có nhận xét là việc thực hiện thao tác của đề bài thì không khác gì việc tăng số bé nhất lên 1 đơn vị và giảm số lớn nhất đi 1 đơn vị. và giải hai bài toán một cách riêng biệt.

## H. Cắt bánh!

Ta dùng công thức QHĐ dp[i][j][k] là cắt miếng bánh cạnh độ dài i,j bằng k nhát sẽ cho cạnh hình vuông độ dài lớn nhất là bao nhiêu, nếu không cắt được thì in là -1. dp[i][j][k] sẽ truy về min(dp[i][p][o],dp[i][j-p][k-o-1]) và min(dp[p][j][o],dp[i-p][j][k-o-1]) với o và p chạy. Trường hợp cơ bản là khi i=j và k=0. Để tính theo công thức trên ta có thể dùng đệ quy có nhớ để tránh làm lại 1 công việc nhiều lần.

#### Độ phức tạp : O(n\*m\*(n+m)\*k^2).

## I. Ăn bánh!

In ra N\*M-1.

#### Độ phức tạp : O(1).

## J. Cây cầu tình bạn

Ta nhận thấy rằng sẽ đưa hai người nhanh nhất sang bên cầu trước. Sau đó ta sẽ xét đưa những người còn lại sang bên kia dùng hai người nhanh nhất. Việc tính có thể sử dụng mảng tổng dồn.

#### Độ phức tạp : O(n).

## K. Hộp quà tình bạn

Ta sắp xếp lại các a[i] theo thứ tự từ bé đến lớn. Kết quả sẽ là tích các max(0,a[i]-i+1).

#### Độ phức tạp : O(n\*log2(n)).

## L. Vùng đất tình bạn

### Cách 1 :

Với mỗi một ô có người thích ta sẽ loang ra. Đảm bảo sẽ không có quá N thao tác loang cho nên vẫn sẽ có thể chạy được.

#### Độ phức tạp : O(N^2).

### Cách 2 :

Tính khoảng cách giữa những người đang thích người khác, từ đó tính ra được những người nào sẽ không được thích bởi ai.

#### Độ phức tạp : O(n).

# Kết thúc
