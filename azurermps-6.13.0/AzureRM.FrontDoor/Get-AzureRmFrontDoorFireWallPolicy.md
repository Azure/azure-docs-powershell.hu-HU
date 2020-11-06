---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499507"
---
# <span data-ttu-id="359d4-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="359d4-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="359d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="359d4-102">SYNOPSIS</span></span>
<span data-ttu-id="359d4-103">A WAF házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="359d4-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="359d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="359d4-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="359d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="359d4-105">DESCRIPTION</span></span>
<span data-ttu-id="359d4-106">A **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet az aktuális előfizetés alatti erőforráscsoport WAF házirendjét kapja.</span><span class="sxs-lookup"><span data-stu-id="359d4-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="359d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="359d4-107">EXAMPLES</span></span>

### <span data-ttu-id="359d4-108">Példa 1: WAF-házirend beszerzése $Name néven $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="359d4-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="359d4-109">A $resourceGroup $Name nevű WAF-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="359d4-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="359d4-110">2. példa: az összes WAF-házirend beszerzése $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="359d4-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="359d4-111">Az összes WAF-házirend beszerzése $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="359d4-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="359d4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="359d4-112">PARAMETERS</span></span>

### <span data-ttu-id="359d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359d4-113">-DefaultProfile</span></span>
<span data-ttu-id="359d4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="359d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="359d4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="359d4-115">-Name</span></span>
<span data-ttu-id="359d4-116">FireWallPolicy neve</span><span class="sxs-lookup"><span data-stu-id="359d4-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="359d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="359d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="359d4-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="359d4-118">The resource group name.</span></span>

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

### <span data-ttu-id="359d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359d4-119">CommonParameters</span></span>
<span data-ttu-id="359d4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="359d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359d4-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="359d4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359d4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="359d4-122">INPUTS</span></span>

### <span data-ttu-id="359d4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="359d4-123">System.String</span></span>

## <span data-ttu-id="359d4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="359d4-124">OUTPUTS</span></span>

### <span data-ttu-id="359d4-125">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="359d4-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="359d4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="359d4-126">NOTES</span></span>

## <span data-ttu-id="359d4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="359d4-127">RELATED LINKS</span></span>

<span data-ttu-id="359d4-128">[Új – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="359d4-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
