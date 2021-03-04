---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920530"
---
# <span data-ttu-id="a1735-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="a1735-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="a1735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1735-102">SYNOPSIS</span></span>
<span data-ttu-id="a1735-103">Állítsa be a megadott eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="a1735-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="a1735-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1735-104">SYNTAX</span></span>

### <span data-ttu-id="a1735-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1735-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1735-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1735-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1735-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1735-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1735-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1735-108">DESCRIPTION</span></span>
<span data-ttu-id="a1735-109">Állítsa be a megadott nem edge-beli eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="a1735-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="a1735-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1735-110">EXAMPLES</span></span>

### <span data-ttu-id="a1735-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a1735-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="a1735-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1735-112">PARAMETERS</span></span>

### <span data-ttu-id="a1735-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1735-113">-DefaultProfile</span></span>
<span data-ttu-id="a1735-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1735-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1735-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a1735-115">-DeviceId</span></span>
<span data-ttu-id="a1735-116">Nem edge-beli eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1735-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="a1735-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1735-117">-Force</span></span>
<span data-ttu-id="a1735-118">Felülírja a nem edge-beli eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="a1735-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="a1735-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1735-119">-InputObject</span></span>
<span data-ttu-id="a1735-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a1735-120">IotHub object</span></span>

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

### <span data-ttu-id="a1735-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a1735-121">-IotHubName</span></span>
<span data-ttu-id="a1735-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a1735-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1735-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="a1735-123">-ParentDeviceId</span></span>
<span data-ttu-id="a1735-124">A peremhálózati eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1735-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1735-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1735-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1735-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a1735-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1735-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1735-127">-ResourceId</span></span>
<span data-ttu-id="a1735-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a1735-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a1735-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1735-129">-Confirm</span></span>
<span data-ttu-id="a1735-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1735-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1735-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1735-131">-WhatIf</span></span>
<span data-ttu-id="a1735-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1735-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1735-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1735-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1735-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1735-134">CommonParameters</span></span>
<span data-ttu-id="a1735-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1735-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1735-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1735-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1735-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1735-137">INPUTS</span></span>

### <span data-ttu-id="a1735-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a1735-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a1735-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a1735-139">System.String</span></span>

## <span data-ttu-id="a1735-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1735-140">OUTPUTS</span></span>

### <span data-ttu-id="a1735-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="a1735-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="a1735-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1735-142">NOTES</span></span>

## <span data-ttu-id="a1735-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1735-143">RELATED LINKS</span></span>
