---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187781"
---
# <span data-ttu-id="6a0c6-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="6a0c6-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="6a0c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0c6-103">A nem szélezett eszközök felvétele gyermekként az Edge-eszközre.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="6a0c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a0c6-104">SYNTAX</span></span>

### <span data-ttu-id="6a0c6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a0c6-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0c6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a0c6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a0c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a0c6-108">DESCRIPTION</span></span>
<span data-ttu-id="6a0c6-109">Adjon meg egy pontosvesszővel elválasztott listát a nem Edge-eszközök azonosítói a megadott Edge-eszköz gyermekeiként.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="6a0c6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a0c6-110">EXAMPLES</span></span>

### <span data-ttu-id="6a0c6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a0c6-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="6a0c6-112">A nem szélezett eszközök felvétele gyermekként az Edge-eszközre.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="6a0c6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6a0c6-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="6a0c6-114">Nem szélezett eszközök felvétele gyermekként az Edge-eszköz függetlenül attól a nem az Edge eszközön már gyermek a másik Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="6a0c6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a0c6-115">PARAMETERS</span></span>

### <span data-ttu-id="6a0c6-116">-Children (gyermekek)</span><span class="sxs-lookup"><span data-stu-id="6a0c6-116">-Children</span></span>
<span data-ttu-id="6a0c6-117">Alárendelt eszközök listája (vesszővel elválasztott): csak a nem él eszközöket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0c6-118">-DefaultProfile</span></span>
<span data-ttu-id="6a0c6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a0c6-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6a0c6-120">-DeviceId</span></span>
<span data-ttu-id="6a0c6-121">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6a0c6-122">-Force</span></span>
<span data-ttu-id="6a0c6-123">Felülírja a nem él eszköz fölérendelt eszközét.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-123">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a0c6-124">-InputObject</span></span>
<span data-ttu-id="6a0c6-125">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="6a0c6-125">IotHub object</span></span>

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

### <span data-ttu-id="6a0c6-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-126">-IotHubName</span></span>
<span data-ttu-id="6a0c6-127">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="6a0c6-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6a0c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a0c6-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6a0c6-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6a0c6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0c6-130">-ResourceId</span></span>
<span data-ttu-id="6a0c6-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="6a0c6-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6a0c6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a0c6-132">-Confirm</span></span>
<span data-ttu-id="6a0c6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0c6-134">-WhatIf</span></span>
<span data-ttu-id="6a0c6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0c6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0c6-137">CommonParameters</span></span>
<span data-ttu-id="6a0c6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a0c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0c6-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0c6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a0c6-140">INPUTS</span></span>

### <span data-ttu-id="6a0c6-141">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6a0c6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6a0c6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6a0c6-142">System.String</span></span>

## <span data-ttu-id="6a0c6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a0c6-143">OUTPUTS</span></span>

### <span data-ttu-id="6a0c6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="6a0c6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="6a0c6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a0c6-145">NOTES</span></span>

## <span data-ttu-id="6a0c6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a0c6-146">RELATED LINKS</span></span>
