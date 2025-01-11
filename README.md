Just install the package
```bash
go get github.com/username/go-ipinfo
```

And use

```go
func main() {
	client := &http.Client{Timeout: 10 * time.Second}
	ip := "8.8.8.8"
	info, err := GetIPInfo(client, ip)
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	fmt.Printf("AS Field: %s\n", info.ASField)
}
```