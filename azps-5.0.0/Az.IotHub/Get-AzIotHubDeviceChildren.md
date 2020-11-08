---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187754"
---
# <span data-ttu-id="fc96f-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fc96f-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="fc96f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc96f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc96f-103">A hozzárendelt alárendelt eszközök pontosvesszővel tagolt listájának nyomtatása.</span><span class="sxs-lookup"><span data-stu-id="fc96f-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="fc96f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc96f-104">SYNTAX</span></span>

### <span data-ttu-id="fc96f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc96f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc96f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc96f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc96f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc96f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc96f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc96f-108">DESCRIPTION</span></span>
<span data-ttu-id="fc96f-109">Az összes hozzárendelt nem élű eszköz megjelenítése pontosvesszővel elválasztott listának az összes Edge-eszközön vagy megadott eszközön.</span><span class="sxs-lookup"><span data-stu-id="fc96f-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="fc96f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc96f-110">EXAMPLES</span></span>

### <span data-ttu-id="fc96f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc96f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="fc96f-112">Pontosvesszővel tagolt listaként jelenítse meg az összes hozzárendelt nem él eszközt.</span><span class="sxs-lookup"><span data-stu-id="fc96f-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="fc96f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fc96f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="fc96f-114">Az összes hozzárendelt nem élű eszköz megjelenítése pontosvesszővel elválasztott listának az összes Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="fc96f-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="fc96f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc96f-115">PARAMETERS</span></span>

### <span data-ttu-id="fc96f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc96f-116">-DefaultProfile</span></span>
<span data-ttu-id="fc96f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc96f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc96f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc96f-118">-DeviceId</span></span>
<span data-ttu-id="fc96f-119">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fc96f-119">Id of edge device.</span></span>

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

### <span data-ttu-id="fc96f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc96f-120">-InputObject</span></span>
<span data-ttu-id="fc96f-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="fc96f-121">IotHub object</span></span>

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

### <span data-ttu-id="fc96f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc96f-122">-IotHubName</span></span>
<span data-ttu-id="fc96f-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="fc96f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc96f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc96f-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc96f-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fc96f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc96f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc96f-126">-ResourceId</span></span>
<span data-ttu-id="fc96f-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fc96f-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc96f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc96f-128">CommonParameters</span></span>
<span data-ttu-id="fc96f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc96f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc96f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc96f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc96f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc96f-131">INPUTS</span></span>

### <span data-ttu-id="fc96f-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc96f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc96f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fc96f-133">System.String</span></span>

## <span data-ttu-id="fc96f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc96f-134">OUTPUTS</span></span>

### <span data-ttu-id="fc96f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fc96f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="fc96f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="fc96f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="fc96f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc96f-137">NOTES</span></span>

## <span data-ttu-id="fc96f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc96f-138">RELATED LINKS</span></span>
