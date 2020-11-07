---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 834a713e5fb7cc6bfcf24244bbb376eb0f01a8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668020"
---
# <span data-ttu-id="f42b2-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="f42b2-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="f42b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f42b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f42b2-103">Létrehozza a példányát `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="f42b2-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="f42b2-104">A tanúsítványt a privát HITELESÍTÉSSZOLGÁLTATÓ bocsáthatja ki, és az API-kezelési szolgáltatásba telepíti, és `CertificateAuthority` az `Root` áruházba kerül.</span><span class="sxs-lookup"><span data-stu-id="f42b2-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="f42b2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f42b2-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f42b2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="f42b2-106">DESCRIPTION</span></span>
<span data-ttu-id="f42b2-107">A **New-AzApiManagementSystemCertificate** parancsmag egy olyan segítő parancs, amely a **PsApiManagementSystemCertificate** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f42b2-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="f42b2-108">Ezt a parancsot a New-AzApiManagement és a Set-AzApiManagement parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="f42b2-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="f42b2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f42b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f42b2-110">Példa 1: PsApiManagementSystemCertificate-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból</span><span class="sxs-lookup"><span data-stu-id="f42b2-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="f42b2-111">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementSystemCertificate** példányát a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="f42b2-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="f42b2-112">Ekkor létrejön és API-kezelési szolgáltatás, amely a HITELESÍTÉSSZOLGÁLTATÓ tanúsítványát telepíti a legfelső szintű tárolónak.</span><span class="sxs-lookup"><span data-stu-id="f42b2-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="f42b2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f42b2-113">PARAMETERS</span></span>

### <span data-ttu-id="f42b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42b2-114">-DefaultProfile</span></span>
<span data-ttu-id="f42b2-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f42b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f42b2-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="f42b2-116">-PfxPassword</span></span>
<span data-ttu-id="f42b2-117">A. pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="f42b2-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="f42b2-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="f42b2-118">-PfxPath</span></span>
<span data-ttu-id="f42b2-119">A. pfx tanúsítványfájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="f42b2-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="f42b2-120">-StoreName mezőt</span><span class="sxs-lookup"><span data-stu-id="f42b2-120">-StoreName</span></span>
<span data-ttu-id="f42b2-121">Tanúsítvány StoreName mezőt</span><span class="sxs-lookup"><span data-stu-id="f42b2-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="f42b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42b2-122">CommonParameters</span></span>
<span data-ttu-id="f42b2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f42b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42b2-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f42b2-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42b2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f42b2-125">INPUTS</span></span>

### <span data-ttu-id="f42b2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f42b2-126">System.String</span></span>

### <span data-ttu-id="f42b2-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f42b2-127">System.Security.SecureString</span></span>

## <span data-ttu-id="f42b2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f42b2-128">OUTPUTS</span></span>

### <span data-ttu-id="f42b2-129">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="f42b2-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="f42b2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f42b2-130">NOTES</span></span>

## <span data-ttu-id="f42b2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f42b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="f42b2-132">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f42b2-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f42b2-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f42b2-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)