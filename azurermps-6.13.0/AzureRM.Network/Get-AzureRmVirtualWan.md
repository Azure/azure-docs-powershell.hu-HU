---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495071"
---
# <span data-ttu-id="de49e-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="de49e-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="de49e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de49e-102">SYNOPSIS</span></span>
<span data-ttu-id="de49e-103">Egy erőforráscsoport vagy-előfizetés virtuális WAN-vagy virtuális WAN-kapcsolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="de49e-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de49e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de49e-104">SYNTAX</span></span>

### <span data-ttu-id="de49e-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de49e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de49e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de49e-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de49e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de49e-107">DESCRIPTION</span></span>
<span data-ttu-id="de49e-108">Egy erőforráscsoport vagy-előfizetés virtuális WAN-vagy virtuális WAN-kapcsolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="de49e-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="de49e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de49e-109">EXAMPLES</span></span>

### <span data-ttu-id="de49e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de49e-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="de49e-111">Ez a parancs a virtuális WAN nevű myVirtualWAN az erőforráscsoport testRG.</span><span class="sxs-lookup"><span data-stu-id="de49e-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="de49e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de49e-112">PARAMETERS</span></span>

### <span data-ttu-id="de49e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de49e-113">-DefaultProfile</span></span>
<span data-ttu-id="de49e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de49e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de49e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de49e-115">-Name</span></span>
<span data-ttu-id="de49e-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="de49e-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de49e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de49e-117">-ResourceGroupName</span></span>
<span data-ttu-id="de49e-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de49e-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de49e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de49e-119">CommonParameters</span></span>
<span data-ttu-id="de49e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de49e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de49e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de49e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de49e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de49e-122">INPUTS</span></span>

### <span data-ttu-id="de49e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="de49e-123">None</span></span>

## <span data-ttu-id="de49e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de49e-124">OUTPUTS</span></span>

### <span data-ttu-id="de49e-125">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="de49e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="de49e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de49e-126">NOTES</span></span>

## <span data-ttu-id="de49e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de49e-127">RELATED LINKS</span></span>
