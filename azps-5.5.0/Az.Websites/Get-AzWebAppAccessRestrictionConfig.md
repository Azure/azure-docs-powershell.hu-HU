---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149698"
---
# <span data-ttu-id="85832-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="85832-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="85832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85832-102">SYNOPSIS</span></span>
<span data-ttu-id="85832-103">Gets Access Restiction configuration for an Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="85832-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="85832-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85832-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85832-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85832-105">DESCRIPTION</span></span>
<span data-ttu-id="85832-106">A **Get-AzWebAppAccessRestrictionConfig** parancsmag access-korlátozási konfigurációt kap egy Azure Web Appról.</span><span class="sxs-lookup"><span data-stu-id="85832-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="85832-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85832-107">EXAMPLES</span></span>

### <span data-ttu-id="85832-108">1. példa: Web App-hozzáférés korlátozási konfigja erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="85832-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="85832-109">Ez a parancs a Default-Web-WestUS erőforráscsoporthoz tartozó ContosoSite nevű webalkalmazás hozzáférési korlátozási konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="85832-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="85832-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85832-110">PARAMETERS</span></span>

### <span data-ttu-id="85832-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85832-111">-DefaultProfile</span></span>
<span data-ttu-id="85832-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85832-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85832-113">-Name</span><span class="sxs-lookup"><span data-stu-id="85832-113">-Name</span></span>
<span data-ttu-id="85832-114">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="85832-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85832-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85832-115">-ResourceGroupName</span></span>
<span data-ttu-id="85832-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="85832-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85832-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="85832-117">-SlotName</span></span>
<span data-ttu-id="85832-118">Az üzembe helyezési hely neve.</span><span class="sxs-lookup"><span data-stu-id="85832-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85832-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85832-119">CommonParameters</span></span>
<span data-ttu-id="85832-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85832-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85832-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85832-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85832-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85832-122">INPUTS</span></span>

### <span data-ttu-id="85832-123">System.String</span><span class="sxs-lookup"><span data-stu-id="85832-123">System.String</span></span>

## <span data-ttu-id="85832-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85832-124">OUTPUTS</span></span>

### <span data-ttu-id="85832-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="85832-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="85832-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85832-126">NOTES</span></span>

## <span data-ttu-id="85832-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85832-127">RELATED LINKS</span></span>

[<span data-ttu-id="85832-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="85832-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="85832-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="85832-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="85832-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="85832-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
