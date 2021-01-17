---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350297"
---
# <span data-ttu-id="9a125-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="9a125-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="9a125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a125-102">SYNOPSIS</span></span>
<span data-ttu-id="9a125-103">Létrehozza a `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="9a125-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="9a125-104">A tanúsítványt a privát hitelesítésszolgáltatók is kibocsáthatja, és az API-kezelési szolgáltatásba telepítve vagy `CertificateAuthority` `Root` tárolva lesznek.</span><span class="sxs-lookup"><span data-stu-id="9a125-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="9a125-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a125-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a125-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a125-106">DESCRIPTION</span></span>
<span data-ttu-id="9a125-107">A **New-AzApiManagementSystemCertificate** parancsmag egy segítő parancs, amely létrehozza a **PsApiManagementSystemCertificate példányát.**</span><span class="sxs-lookup"><span data-stu-id="9a125-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="9a125-108">Ez a parancs a parancsmaggal New-AzApiManagement és Set-AzApiManagement is használható.</span><span class="sxs-lookup"><span data-stu-id="9a125-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="9a125-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a125-109">EXAMPLES</span></span>

### <span data-ttu-id="9a125-110">1. példa: A PsApiManagementSystemCertificate példány létrehozása és inicializálása ssl-tanúsítvány használatával fájlból</span><span class="sxs-lookup"><span data-stu-id="9a125-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="9a125-111">Ez a parancs létrehozza és inicializálja a **PsApiManagementSystemCertificate** egy példányát egy legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="9a125-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="9a125-112">Ezután létrehozza és API-kezelő szolgáltatást hoz létre, amely telepíti a hitelesítésszolgáltatói tanúsítványt a gyökértárba.</span><span class="sxs-lookup"><span data-stu-id="9a125-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="9a125-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a125-113">PARAMETERS</span></span>

### <span data-ttu-id="9a125-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a125-114">-DefaultProfile</span></span>
<span data-ttu-id="9a125-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a125-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a125-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="9a125-116">-PfxPassword</span></span>
<span data-ttu-id="9a125-117">A .pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="9a125-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a125-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="9a125-118">-PfxPath</span></span>
<span data-ttu-id="9a125-119">A .pfx tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9a125-119">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a125-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="9a125-120">-StoreName</span></span>
<span data-ttu-id="9a125-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="9a125-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a125-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a125-122">CommonParameters</span></span>
<span data-ttu-id="9a125-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a125-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a125-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a125-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a125-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a125-125">INPUTS</span></span>

### <span data-ttu-id="9a125-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9a125-126">System.String</span></span>

### <span data-ttu-id="9a125-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="9a125-127">System.Security.SecureString</span></span>

## <span data-ttu-id="9a125-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a125-128">OUTPUTS</span></span>

### <span data-ttu-id="9a125-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="9a125-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="9a125-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a125-130">NOTES</span></span>

## <span data-ttu-id="9a125-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a125-131">RELATED LINKS</span></span>

[<span data-ttu-id="9a125-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a125-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="9a125-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a125-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)