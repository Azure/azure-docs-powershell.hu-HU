---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845758"
---
# <span data-ttu-id="f9fbd-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f9fbd-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="f9fbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fbd-103">Az Azure Web App elérési restiction-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="f9fbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9fbd-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9fbd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fbd-106">A **Get-AzWebAppAccessRestrictionConfig** parancsmag hozzáférést kap az Azure Web App alkalmazással kapcsolatos korlátozási konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="f9fbd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fbd-108">Példa 1: webalkalmazás hozzáférés-korlátozási konfigurációjának beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="f9fbd-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f9fbd-109">Ez a parancs a ContosoSite nevű webalkalmazás hozzáférés korlátozási konfigurációját kapja meg, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f9fbd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="f9fbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fbd-111">-DefaultProfile</span></span>
<span data-ttu-id="f9fbd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9fbd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9fbd-113">-Name</span></span>
<span data-ttu-id="f9fbd-114">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f9fbd-114">WebApp Name</span></span>

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

### <span data-ttu-id="f9fbd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fbd-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9fbd-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f9fbd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f9fbd-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="f9fbd-117">-SlotName</span></span>
<span data-ttu-id="f9fbd-118">A telepítő tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="f9fbd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fbd-119">CommonParameters</span></span>
<span data-ttu-id="f9fbd-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9fbd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fbd-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fbd-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9fbd-122">INPUTS</span></span>

### <span data-ttu-id="f9fbd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f9fbd-123">System.String</span></span>

## <span data-ttu-id="f9fbd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9fbd-124">OUTPUTS</span></span>

### <span data-ttu-id="f9fbd-125">Microsoft. Azure. Command. WebApps. models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f9fbd-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="f9fbd-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9fbd-126">NOTES</span></span>

## <span data-ttu-id="f9fbd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9fbd-127">RELATED LINKS</span></span>

[<span data-ttu-id="f9fbd-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f9fbd-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="f9fbd-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f9fbd-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="f9fbd-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f9fbd-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
