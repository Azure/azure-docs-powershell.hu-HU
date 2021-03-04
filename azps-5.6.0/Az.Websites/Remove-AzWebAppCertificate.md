---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933474"
---
# <span data-ttu-id="9151f-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="9151f-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="9151f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9151f-102">SYNOPSIS</span></span>
<span data-ttu-id="9151f-103">Eltávolít egy Appszolgáltatás által felügyelt tanúsítványt egy Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="9151f-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="9151f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9151f-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9151f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9151f-105">DESCRIPTION</span></span>
<span data-ttu-id="9151f-106">A **Remove-AzWebAppCertificate** parancsmag eltávolítja az Azure App Service Felügyelt tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="9151f-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="9151f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9151f-107">EXAMPLES</span></span>

### <span data-ttu-id="9151f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9151f-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="9151f-109">Ez a parancs eltávolítja az appszolgáltatás által felügyelt tanúsítványt az adott webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="9151f-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="9151f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9151f-110">PARAMETERS</span></span>

### <span data-ttu-id="9151f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9151f-111">-DefaultProfile</span></span>
<span data-ttu-id="9151f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9151f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9151f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9151f-113">-ResourceGroupName</span></span>
<span data-ttu-id="9151f-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9151f-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9151f-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="9151f-115">-ThumbPrint</span></span>
<span data-ttu-id="9151f-116">A webtérben már megtalálható tanúsítvány thumbprint of the certificate that already exists in web space.</span><span class="sxs-lookup"><span data-stu-id="9151f-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9151f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9151f-117">CommonParameters</span></span>
<span data-ttu-id="9151f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9151f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9151f-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9151f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9151f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9151f-120">INPUTS</span></span>

### <span data-ttu-id="9151f-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="9151f-121">None</span></span>

## <span data-ttu-id="9151f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9151f-122">OUTPUTS</span></span>

### <span data-ttu-id="9151f-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="9151f-123">System.Void</span></span>

## <span data-ttu-id="9151f-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9151f-124">NOTES</span></span>

## <span data-ttu-id="9151f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9151f-125">RELATED LINKS</span></span>
[<span data-ttu-id="9151f-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="9151f-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
