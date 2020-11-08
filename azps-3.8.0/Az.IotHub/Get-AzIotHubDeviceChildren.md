---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011683"
---
# <span data-ttu-id="a4ad0-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a4ad0-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="a4ad0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ad0-103">A hozzárendelt alárendelt eszközök pontosvesszővel tagolt listájának nyomtatása.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="a4ad0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4ad0-104">SYNTAX</span></span>

### <span data-ttu-id="a4ad0-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4ad0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ad0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4ad0-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ad0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4ad0-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ad0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4ad0-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ad0-109">Az összes hozzárendelt nem élű eszköz megjelenítése pontosvesszővel elválasztott listának az összes Edge-eszközön vagy megadott eszközön.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="a4ad0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4ad0-110">EXAMPLES</span></span>

### <span data-ttu-id="a4ad0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4ad0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="a4ad0-112">Pontosvesszővel tagolt listaként jelenítse meg az összes hozzárendelt nem él eszközt.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="a4ad0-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a4ad0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="a4ad0-114">Az összes hozzárendelt nem élű eszköz megjelenítése pontosvesszővel elválasztott listának az összes Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="a4ad0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4ad0-115">PARAMETERS</span></span>

### <span data-ttu-id="a4ad0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ad0-116">-DefaultProfile</span></span>
<span data-ttu-id="a4ad0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ad0-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a4ad0-118">-DeviceId</span></span>
<span data-ttu-id="a4ad0-119">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4ad0-119">Id of edge device.</span></span>

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

### <span data-ttu-id="a4ad0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ad0-120">-InputObject</span></span>
<span data-ttu-id="a4ad0-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a4ad0-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ad0-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a4ad0-122">-IotHubName</span></span>
<span data-ttu-id="a4ad0-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a4ad0-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ad0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ad0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4ad0-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a4ad0-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ad0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ad0-126">-ResourceId</span></span>
<span data-ttu-id="a4ad0-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a4ad0-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ad0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ad0-128">CommonParameters</span></span>
<span data-ttu-id="a4ad0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4ad0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ad0-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ad0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ad0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ad0-131">INPUTS</span></span>

### <span data-ttu-id="a4ad0-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a4ad0-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a4ad0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ad0-133">System.String</span></span>

## <span data-ttu-id="a4ad0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ad0-134">OUTPUTS</span></span>

### <span data-ttu-id="a4ad0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a4ad0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="a4ad0-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="a4ad0-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="a4ad0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4ad0-137">NOTES</span></span>

## <span data-ttu-id="a4ad0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4ad0-138">RELATED LINKS</span></span>
