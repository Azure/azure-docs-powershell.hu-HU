---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 432e6ce1562a7f341cc9e121e1012354c5c67a93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842149"
---
# <span data-ttu-id="1a5af-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a5af-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1a5af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a5af-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5af-103">Visszakapja a tanúsítvány állapotát.</span><span class="sxs-lookup"><span data-stu-id="1a5af-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="1a5af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a5af-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a5af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a5af-105">DESCRIPTION</span></span>
<span data-ttu-id="1a5af-106">A **Get-AzKeyVaultCertificateOperation** parancsmag egy tanúsítvány-művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1a5af-106">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="1a5af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a5af-107">EXAMPLES</span></span>

### <span data-ttu-id="1a5af-108">Példa 1: tanúsítvány-művelet állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1a5af-108">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="1a5af-109">Ez a parancs a ContosoKV01 TestCert01 tanúsítványának állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1a5af-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1a5af-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a5af-110">PARAMETERS</span></span>

### <span data-ttu-id="1a5af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5af-111">-DefaultProfile</span></span>
<span data-ttu-id="1a5af-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1a5af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a5af-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a5af-113">-Name</span></span>
<span data-ttu-id="1a5af-114">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a5af-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5af-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1a5af-115">-VaultName</span></span>
<span data-ttu-id="1a5af-116">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a5af-116">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5af-117">CommonParameters</span></span>
<span data-ttu-id="1a5af-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a5af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5af-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5af-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5af-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a5af-120">INPUTS</span></span>

### <span data-ttu-id="1a5af-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="1a5af-121">None</span></span>
<span data-ttu-id="1a5af-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1a5af-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a5af-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a5af-123">OUTPUTS</span></span>

### <span data-ttu-id="1a5af-124">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="1a5af-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1a5af-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a5af-125">NOTES</span></span>

## <span data-ttu-id="1a5af-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a5af-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a5af-127">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a5af-127">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="1a5af-128">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a5af-128">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

