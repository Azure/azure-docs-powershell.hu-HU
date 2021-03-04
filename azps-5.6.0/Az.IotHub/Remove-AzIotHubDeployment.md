---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: a125bd402a58bc138e1fa74ec2f68d659f2a1d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928009"
---
# <span data-ttu-id="5cf21-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="5cf21-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="5cf21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf21-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf21-103">IoT Edge-telepítés törlése.</span><span class="sxs-lookup"><span data-stu-id="5cf21-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="5cf21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5cf21-104">SYNTAX</span></span>

### <span data-ttu-id="5cf21-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5cf21-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf21-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5cf21-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf21-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5cf21-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf21-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5cf21-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf21-109">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="5cf21-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="5cf21-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5cf21-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf21-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5cf21-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="5cf21-112">IoT Edge-telepítés törlése.</span><span class="sxs-lookup"><span data-stu-id="5cf21-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="5cf21-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cf21-113">PARAMETERS</span></span>

### <span data-ttu-id="5cf21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf21-114">-DefaultProfile</span></span>
<span data-ttu-id="5cf21-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cf21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf21-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cf21-116">-InputObject</span></span>
<span data-ttu-id="5cf21-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5cf21-117">IotHub object</span></span>

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

### <span data-ttu-id="5cf21-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5cf21-118">-IotHubName</span></span>
<span data-ttu-id="5cf21-119">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="5cf21-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5cf21-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5cf21-120">-Name</span></span>
<span data-ttu-id="5cf21-121">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5cf21-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="5cf21-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cf21-122">-PassThru</span></span>
<span data-ttu-id="5cf21-123">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="5cf21-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="5cf21-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5cf21-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5cf21-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf21-125">-ResourceGroupName</span></span>
<span data-ttu-id="5cf21-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5cf21-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5cf21-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf21-127">-ResourceId</span></span>
<span data-ttu-id="5cf21-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5cf21-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5cf21-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cf21-129">-Confirm</span></span>
<span data-ttu-id="5cf21-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5cf21-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf21-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf21-131">-WhatIf</span></span>
<span data-ttu-id="5cf21-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5cf21-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf21-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cf21-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf21-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf21-134">CommonParameters</span></span>
<span data-ttu-id="5cf21-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf21-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf21-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf21-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cf21-137">INPUTS</span></span>

### <span data-ttu-id="5cf21-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5cf21-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5cf21-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5cf21-139">System.String</span></span>

## <span data-ttu-id="5cf21-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf21-140">OUTPUTS</span></span>

### <span data-ttu-id="5cf21-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cf21-141">System.Boolean</span></span>

## <span data-ttu-id="5cf21-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5cf21-142">NOTES</span></span>

## <span data-ttu-id="5cf21-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cf21-143">RELATED LINKS</span></span>
