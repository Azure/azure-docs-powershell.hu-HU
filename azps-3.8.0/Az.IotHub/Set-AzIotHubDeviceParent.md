---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011415"
---
# <span data-ttu-id="460ce-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="460ce-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="460ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="460ce-102">SYNOPSIS</span></span>
<span data-ttu-id="460ce-103">A megadott eszköz fölérendelt eszközének beállítása.</span><span class="sxs-lookup"><span data-stu-id="460ce-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="460ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="460ce-104">SYNTAX</span></span>

### <span data-ttu-id="460ce-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="460ce-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="460ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="460ce-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="460ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="460ce-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="460ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="460ce-108">DESCRIPTION</span></span>
<span data-ttu-id="460ce-109">Állítsa be a megadott nem szélezett eszköz fölérendelt eszközét.</span><span class="sxs-lookup"><span data-stu-id="460ce-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="460ce-110">Példák</span><span class="sxs-lookup"><span data-stu-id="460ce-110">EXAMPLES</span></span>

### <span data-ttu-id="460ce-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="460ce-111">Example 1</span></span>
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

## <span data-ttu-id="460ce-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="460ce-112">PARAMETERS</span></span>

### <span data-ttu-id="460ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460ce-113">-DefaultProfile</span></span>
<span data-ttu-id="460ce-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="460ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="460ce-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="460ce-115">-DeviceId</span></span>
<span data-ttu-id="460ce-116">A nem él eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="460ce-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="460ce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="460ce-117">-Force</span></span>
<span data-ttu-id="460ce-118">Felülírja a nem él eszköz fölérendelt eszközét.</span><span class="sxs-lookup"><span data-stu-id="460ce-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="460ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="460ce-119">-InputObject</span></span>
<span data-ttu-id="460ce-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="460ce-120">IotHub object</span></span>

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

### <span data-ttu-id="460ce-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="460ce-121">-IotHubName</span></span>
<span data-ttu-id="460ce-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="460ce-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="460ce-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="460ce-123">-ParentDeviceId</span></span>
<span data-ttu-id="460ce-124">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="460ce-124">Id of edge device.</span></span>

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

### <span data-ttu-id="460ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="460ce-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="460ce-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="460ce-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="460ce-127">-ResourceId</span></span>
<span data-ttu-id="460ce-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="460ce-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="460ce-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="460ce-129">-Confirm</span></span>
<span data-ttu-id="460ce-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="460ce-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460ce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460ce-131">-WhatIf</span></span>
<span data-ttu-id="460ce-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="460ce-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="460ce-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="460ce-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460ce-134">CommonParameters</span></span>
<span data-ttu-id="460ce-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="460ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460ce-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460ce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460ce-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="460ce-137">INPUTS</span></span>

### <span data-ttu-id="460ce-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="460ce-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="460ce-139">System. String</span><span class="sxs-lookup"><span data-stu-id="460ce-139">System.String</span></span>

## <span data-ttu-id="460ce-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="460ce-140">OUTPUTS</span></span>

### <span data-ttu-id="460ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="460ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="460ce-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="460ce-142">NOTES</span></span>

## <span data-ttu-id="460ce-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="460ce-143">RELATED LINKS</span></span>
