---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185329"
---
# <span data-ttu-id="11328-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="11328-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="11328-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11328-102">SYNOPSIS</span></span>
<span data-ttu-id="11328-103">IoT-alapú központi példány törlése</span><span class="sxs-lookup"><span data-stu-id="11328-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="11328-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11328-104">SYNTAX</span></span>

### <span data-ttu-id="11328-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11328-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11328-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11328-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11328-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11328-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11328-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11328-108">DESCRIPTION</span></span>
<span data-ttu-id="11328-109"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="11328-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="11328-110">Példák</span><span class="sxs-lookup"><span data-stu-id="11328-110">EXAMPLES</span></span>

### <span data-ttu-id="11328-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11328-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="11328-112">IoT-alapú központi példány törlése</span><span class="sxs-lookup"><span data-stu-id="11328-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="11328-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11328-113">PARAMETERS</span></span>

### <span data-ttu-id="11328-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11328-114">-DefaultProfile</span></span>
<span data-ttu-id="11328-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11328-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11328-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11328-116">-InputObject</span></span>
<span data-ttu-id="11328-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="11328-117">IotHub object</span></span>

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

### <span data-ttu-id="11328-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="11328-118">-IotHubName</span></span>
<span data-ttu-id="11328-119">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="11328-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="11328-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11328-120">-Name</span></span>
<span data-ttu-id="11328-121">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="11328-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="11328-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11328-122">-PassThru</span></span>
<span data-ttu-id="11328-123">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="11328-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="11328-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="11328-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11328-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11328-125">-ResourceGroupName</span></span>
<span data-ttu-id="11328-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="11328-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11328-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11328-127">-ResourceId</span></span>
<span data-ttu-id="11328-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="11328-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="11328-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11328-129">-Confirm</span></span>
<span data-ttu-id="11328-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11328-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11328-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11328-131">-WhatIf</span></span>
<span data-ttu-id="11328-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11328-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11328-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11328-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11328-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11328-134">CommonParameters</span></span>
<span data-ttu-id="11328-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11328-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11328-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11328-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11328-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11328-137">INPUTS</span></span>

### <span data-ttu-id="11328-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="11328-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="11328-139">System. String</span><span class="sxs-lookup"><span data-stu-id="11328-139">System.String</span></span>

## <span data-ttu-id="11328-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11328-140">OUTPUTS</span></span>

### <span data-ttu-id="11328-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11328-141">System.Boolean</span></span>

## <span data-ttu-id="11328-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11328-142">NOTES</span></span>

## <span data-ttu-id="11328-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11328-143">RELATED LINKS</span></span>
