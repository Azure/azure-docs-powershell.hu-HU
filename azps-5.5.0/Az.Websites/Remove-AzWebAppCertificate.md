---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149666"
---
# <span data-ttu-id="f42ff-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f42ff-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="f42ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f42ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f42ff-103">Létrehoz egy appszolgáltatás által felügyelt tanúsítványt egy Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="f42ff-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="f42ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f42ff-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f42ff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f42ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f42ff-106">A **Remove-AzWebAppCertificate** parancsmag létrehoz egy Azure App Service Felügyelt tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="f42ff-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="f42ff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f42ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f42ff-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f42ff-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="f42ff-109">Ez a parancs eltávolítja az appszolgáltatás által felügyelt tanúsítványt az adott webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="f42ff-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="f42ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f42ff-110">PARAMETERS</span></span>

### <span data-ttu-id="f42ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42ff-111">-DefaultProfile</span></span>
<span data-ttu-id="f42ff-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f42ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f42ff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f42ff-113">-ResourceGroupName</span></span>
<span data-ttu-id="f42ff-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f42ff-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f42ff-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="f42ff-115">-ThumbPrint</span></span>
<span data-ttu-id="f42ff-116">A webtérben már megtalálható tanúsítvány thumbprint of the certificate that already exists in web space.</span><span class="sxs-lookup"><span data-stu-id="f42ff-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="f42ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42ff-117">CommonParameters</span></span>
<span data-ttu-id="f42ff-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f42ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42ff-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f42ff-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42ff-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f42ff-120">INPUTS</span></span>

### <span data-ttu-id="f42ff-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f42ff-121">None</span></span>

## <span data-ttu-id="f42ff-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f42ff-122">OUTPUTS</span></span>

### <span data-ttu-id="f42ff-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="f42ff-123">System.Void</span></span>

## <span data-ttu-id="f42ff-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f42ff-124">NOTES</span></span>

## <span data-ttu-id="f42ff-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f42ff-125">RELATED LINKS</span></span>
[<span data-ttu-id="f42ff-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f42ff-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
