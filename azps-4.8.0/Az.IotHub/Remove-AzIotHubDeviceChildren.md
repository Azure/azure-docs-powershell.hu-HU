---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018235"
---
# <span data-ttu-id="45835-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="45835-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="45835-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45835-102">SYNOPSIS</span></span>
<span data-ttu-id="45835-103">A nem szélezett eszközök eltávolítása gyermekként a megadott Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="45835-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="45835-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45835-104">SYNTAX</span></span>

### <span data-ttu-id="45835-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45835-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45835-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45835-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45835-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45835-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45835-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="45835-108">DESCRIPTION</span></span>
<span data-ttu-id="45835-109">Távolítsa el az összes vagy a fent említett nem szélezett eszközöket a gyermekek által megadott Edge eszközként.</span><span class="sxs-lookup"><span data-stu-id="45835-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="45835-110">Példák</span><span class="sxs-lookup"><span data-stu-id="45835-110">EXAMPLES</span></span>

### <span data-ttu-id="45835-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45835-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="45835-112">Az említett eszközök eltávolítása adott eszköz gyermekeiként</span><span class="sxs-lookup"><span data-stu-id="45835-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="45835-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="45835-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="45835-114">Az összes nem szélezett eszköz eltávolítása a gyermekek által megadott Edge-eszközként.</span><span class="sxs-lookup"><span data-stu-id="45835-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="45835-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45835-115">PARAMETERS</span></span>

### <span data-ttu-id="45835-116">-Children (gyermekek)</span><span class="sxs-lookup"><span data-stu-id="45835-116">-Children</span></span>
<span data-ttu-id="45835-117">Alárendelt eszközök listája (vesszővel elválasztott): csak a nem él eszközöket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="45835-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45835-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45835-118">-DefaultProfile</span></span>
<span data-ttu-id="45835-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45835-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45835-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="45835-120">-DeviceId</span></span>
<span data-ttu-id="45835-121">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45835-121">Id of edge device.</span></span>

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

### <span data-ttu-id="45835-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45835-122">-InputObject</span></span>
<span data-ttu-id="45835-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="45835-123">IotHub object</span></span>

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

### <span data-ttu-id="45835-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="45835-124">-IotHubName</span></span>
<span data-ttu-id="45835-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="45835-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="45835-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45835-126">-PassThru</span></span>
<span data-ttu-id="45835-127">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="45835-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="45835-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="45835-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45835-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45835-129">-ResourceGroupName</span></span>
<span data-ttu-id="45835-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="45835-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="45835-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45835-131">-ResourceId</span></span>
<span data-ttu-id="45835-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="45835-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="45835-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45835-133">-Confirm</span></span>
<span data-ttu-id="45835-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45835-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45835-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45835-135">-WhatIf</span></span>
<span data-ttu-id="45835-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45835-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45835-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45835-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45835-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45835-138">CommonParameters</span></span>
<span data-ttu-id="45835-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45835-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45835-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45835-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45835-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45835-141">INPUTS</span></span>

### <span data-ttu-id="45835-142">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="45835-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="45835-143">System. String</span><span class="sxs-lookup"><span data-stu-id="45835-143">System.String</span></span>

## <span data-ttu-id="45835-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45835-144">OUTPUTS</span></span>

### <span data-ttu-id="45835-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45835-145">System.Boolean</span></span>

## <span data-ttu-id="45835-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45835-146">NOTES</span></span>

## <span data-ttu-id="45835-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45835-147">RELATED LINKS</span></span>
