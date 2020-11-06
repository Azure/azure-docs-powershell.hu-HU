---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492083"
---
# <span data-ttu-id="91dd3-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="91dd3-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="91dd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="91dd3-103">Létrehozza a példányát `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="91dd3-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="91dd3-104">A tanúsítványt a privát HITELESÍTÉSSZOLGÁLTATÓ bocsáthatja ki, és az API-kezelési szolgáltatásba telepíti, és `CertificateAuthority` az `Root` áruházba kerül.</span><span class="sxs-lookup"><span data-stu-id="91dd3-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91dd3-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91dd3-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91dd3-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="91dd3-106">DESCRIPTION</span></span>
<span data-ttu-id="91dd3-107">A **New-AzureRmApiManagementSystemCertificate** parancsmag egy olyan segítő parancs, amely a **PsApiManagementSystemCertificate** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="91dd3-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="91dd3-108">Ezt a parancsot a New-AzureRmApiManagement és a Set-AzureRmApiManagement parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="91dd3-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="91dd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="91dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="91dd3-110">Példa 1: PsApiManagementSystemCertificate-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból</span><span class="sxs-lookup"><span data-stu-id="91dd3-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="91dd3-111">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementSystemCertificate** példányát a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="91dd3-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="91dd3-112">Ekkor létrejön és API-kezelési szolgáltatás, amely a HITELESÍTÉSSZOLGÁLTATÓ tanúsítványát telepíti a legfelső szintű tárolónak.</span><span class="sxs-lookup"><span data-stu-id="91dd3-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="91dd3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91dd3-113">PARAMETERS</span></span>

### <span data-ttu-id="91dd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dd3-114">-DefaultProfile</span></span>
<span data-ttu-id="91dd3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91dd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91dd3-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="91dd3-116">-PfxPassword</span></span>
<span data-ttu-id="91dd3-117">A. pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="91dd3-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="91dd3-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="91dd3-118">-PfxPath</span></span>
<span data-ttu-id="91dd3-119">A. pfx tanúsítványfájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="91dd3-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="91dd3-120">-StoreName mezőt</span><span class="sxs-lookup"><span data-stu-id="91dd3-120">-StoreName</span></span>
<span data-ttu-id="91dd3-121">Tanúsítvány StoreName mezőt</span><span class="sxs-lookup"><span data-stu-id="91dd3-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="91dd3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dd3-122">CommonParameters</span></span>
<span data-ttu-id="91dd3-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91dd3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dd3-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91dd3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dd3-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91dd3-125">INPUTS</span></span>

### <span data-ttu-id="91dd3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="91dd3-126">System.String</span></span>

### <span data-ttu-id="91dd3-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="91dd3-127">System.Security.SecureString</span></span>

## <span data-ttu-id="91dd3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91dd3-128">OUTPUTS</span></span>

### <span data-ttu-id="91dd3-129">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="91dd3-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="91dd3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91dd3-130">NOTES</span></span>

## <span data-ttu-id="91dd3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91dd3-131">RELATED LINKS</span></span>

[<span data-ttu-id="91dd3-132">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="91dd3-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="91dd3-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="91dd3-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
