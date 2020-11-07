---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 60d6263d3fb074cf4795379ae28f1824dc81a4c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666431"
---
# <span data-ttu-id="0be70-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="0be70-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="0be70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0be70-102">SYNOPSIS</span></span>
<span data-ttu-id="0be70-103">A WAF házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="0be70-103">Get WAF policy</span></span>

## <span data-ttu-id="0be70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0be70-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be70-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0be70-105">DESCRIPTION</span></span>
<span data-ttu-id="0be70-106">A **Get-AzFrontDoorWafPolicy** cmdletGet az aktuális előfizetés alatti erőforráscsoport WAF házirendjét kapja.</span><span class="sxs-lookup"><span data-stu-id="0be70-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="0be70-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0be70-107">EXAMPLES</span></span>

### <span data-ttu-id="0be70-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0be70-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="0be70-109">A $resourceGroupName $policyName nevű WAF-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="0be70-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="0be70-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0be70-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="0be70-111">Az összes WAF-házirend beszerzése $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be70-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="0be70-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0be70-112">PARAMETERS</span></span>

### <span data-ttu-id="0be70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be70-113">-DefaultProfile</span></span>
<span data-ttu-id="0be70-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0be70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be70-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0be70-115">-Name</span></span>
<span data-ttu-id="0be70-116">FireWallPolicy neve</span><span class="sxs-lookup"><span data-stu-id="0be70-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be70-117">-ResourceGroupName</span></span>
<span data-ttu-id="0be70-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0be70-118">The resource group name.</span></span>

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

### <span data-ttu-id="0be70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be70-119">CommonParameters</span></span>
<span data-ttu-id="0be70-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0be70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be70-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0be70-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be70-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0be70-122">INPUTS</span></span>

### <span data-ttu-id="0be70-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0be70-123">None</span></span>

## <span data-ttu-id="0be70-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0be70-124">OUTPUTS</span></span>

### <span data-ttu-id="0be70-125">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0be70-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="0be70-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0be70-126">NOTES</span></span>

## <span data-ttu-id="0be70-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0be70-127">RELATED LINKS</span></span>

<span data-ttu-id="0be70-128">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="0be70-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
