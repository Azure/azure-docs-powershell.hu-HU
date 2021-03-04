---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942530"
---
# <span data-ttu-id="70169-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="70169-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="70169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70169-102">SYNOPSIS</span></span>
<span data-ttu-id="70169-103">Vegye fel a nem edge-beli eszközöket gyermekekként a peremeszközökre.</span><span class="sxs-lookup"><span data-stu-id="70169-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="70169-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70169-104">SYNTAX</span></span>

### <span data-ttu-id="70169-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70169-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70169-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70169-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70169-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="70169-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70169-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70169-108">DESCRIPTION</span></span>
<span data-ttu-id="70169-109">Adja hozzá a nem edge-beli eszközazonosítók megadott vesszővel elválasztott listáját a megadott éleszköz gyermekeiként.</span><span class="sxs-lookup"><span data-stu-id="70169-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="70169-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70169-110">EXAMPLES</span></span>

### <span data-ttu-id="70169-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="70169-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="70169-112">Vegye fel a nem edge-beli eszközöket gyermekekként a peremeszközökre.</span><span class="sxs-lookup"><span data-stu-id="70169-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="70169-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="70169-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="70169-114">Gyermekként felvehet nem edge-eszközöket a peremeszközökre, függetlenül attól, hogy a nem edge típusú eszköz már egy másik edge-eszköz gyermeke.</span><span class="sxs-lookup"><span data-stu-id="70169-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="70169-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70169-115">PARAMETERS</span></span>

### <span data-ttu-id="70169-116">-Gyermekek</span><span class="sxs-lookup"><span data-stu-id="70169-116">-Children</span></span>
<span data-ttu-id="70169-117">A gyermekeszköz-lista (vesszővel elválasztva) csak a nem edge-eszközökhöz használható.</span><span class="sxs-lookup"><span data-stu-id="70169-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="70169-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70169-118">-DefaultProfile</span></span>
<span data-ttu-id="70169-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70169-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70169-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="70169-120">-DeviceId</span></span>
<span data-ttu-id="70169-121">A peremhálózati eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="70169-121">Id of edge device.</span></span>

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

### <span data-ttu-id="70169-122">-Force</span><span class="sxs-lookup"><span data-stu-id="70169-122">-Force</span></span>
<span data-ttu-id="70169-123">Felülírja a nem edge-beli eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="70169-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="70169-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70169-124">-InputObject</span></span>
<span data-ttu-id="70169-125">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="70169-125">IotHub object</span></span>

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

### <span data-ttu-id="70169-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="70169-126">-IotHubName</span></span>
<span data-ttu-id="70169-127">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="70169-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="70169-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70169-128">-ResourceGroupName</span></span>
<span data-ttu-id="70169-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="70169-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70169-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70169-130">-ResourceId</span></span>
<span data-ttu-id="70169-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="70169-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="70169-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70169-132">-Confirm</span></span>
<span data-ttu-id="70169-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70169-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70169-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70169-134">-WhatIf</span></span>
<span data-ttu-id="70169-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70169-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70169-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70169-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70169-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70169-137">CommonParameters</span></span>
<span data-ttu-id="70169-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70169-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70169-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70169-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70169-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70169-140">INPUTS</span></span>

### <span data-ttu-id="70169-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="70169-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="70169-142">System.String</span><span class="sxs-lookup"><span data-stu-id="70169-142">System.String</span></span>

## <span data-ttu-id="70169-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70169-143">OUTPUTS</span></span>

### <span data-ttu-id="70169-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Minden</span><span class="sxs-lookup"><span data-stu-id="70169-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="70169-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70169-145">NOTES</span></span>

## <span data-ttu-id="70169-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70169-146">RELATED LINKS</span></span>
