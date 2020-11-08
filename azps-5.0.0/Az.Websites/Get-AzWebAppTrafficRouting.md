---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187120"
---
# <span data-ttu-id="a48e6-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a48e6-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="a48e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a48e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a48e6-103">A megadott bővítőhelyhez tartozó útválasztási szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="a48e6-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="a48e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a48e6-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a48e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a48e6-105">DESCRIPTION</span></span>
<span data-ttu-id="a48e6-106">A **Get-AzWebAppTrafficRouting** parancsmag az Azure Web App-bővítőhelyről kapja meg az útválasztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a48e6-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="a48e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a48e6-107">EXAMPLES</span></span>

### <span data-ttu-id="a48e6-108">Példa 1 az adott útválasztási szabály beolvasása a WebApp bővítőhelyről</span><span class="sxs-lookup"><span data-stu-id="a48e6-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="a48e6-109">Ez a parancs az adott WebApp-bővítőhelyhez tartozó útválasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a48e6-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="a48e6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a48e6-110">PARAMETERS</span></span>

### <span data-ttu-id="a48e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48e6-111">-DefaultProfile</span></span>
<span data-ttu-id="a48e6-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a48e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a48e6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48e6-113">-ResourceGroupName</span></span>
<span data-ttu-id="a48e6-114">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a48e6-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e6-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a48e6-115">-RuleName</span></span>
<span data-ttu-id="a48e6-116">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="a48e6-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e6-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a48e6-117">-WebAppName</span></span>
<span data-ttu-id="a48e6-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a48e6-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48e6-119">CommonParameters</span></span>
<span data-ttu-id="a48e6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a48e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48e6-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a48e6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48e6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a48e6-122">INPUTS</span></span>

### <span data-ttu-id="a48e6-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="a48e6-123">None</span></span>

## <span data-ttu-id="a48e6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a48e6-124">OUTPUTS</span></span>

### <span data-ttu-id="a48e6-125">Microsoft. Azure. Management. WebSites. models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="a48e6-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="a48e6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a48e6-126">NOTES</span></span>

## <span data-ttu-id="a48e6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a48e6-127">RELATED LINKS</span></span>

[<span data-ttu-id="a48e6-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a48e6-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a48e6-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a48e6-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a48e6-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a48e6-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)