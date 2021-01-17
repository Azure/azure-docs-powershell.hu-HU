---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337302"
---
# <span data-ttu-id="4ba15-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ba15-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="4ba15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba15-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba15-103">Eszköz biztonsági csoportjának törlése</span><span class="sxs-lookup"><span data-stu-id="4ba15-103">Delete device security group</span></span>

## <span data-ttu-id="4ba15-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ba15-104">SYNTAX</span></span>

### <span data-ttu-id="4ba15-105">ResourceIdLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ba15-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba15-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba15-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba15-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba15-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ba15-108">DESCRIPTION</span></span>
<span data-ttu-id="4ba15-109">A Remove-AzDeviceSecurityGroup parancsmag törli az iot biztonsági megoldásban definiált eszközbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="4ba15-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="4ba15-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ba15-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba15-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4ba15-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="4ba15-112">Törölje az iot hub "MySecurityGroup" eszközbiztonsági csoportját az "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="4ba15-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="4ba15-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ba15-113">PARAMETERS</span></span>

### <span data-ttu-id="4ba15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba15-114">-DefaultProfile</span></span>
<span data-ttu-id="4ba15-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ba15-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba15-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba15-116">-HubResourceId</span></span>
<span data-ttu-id="4ba15-117">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="4ba15-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba15-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba15-118">-InputObject</span></span>
<span data-ttu-id="4ba15-119">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="4ba15-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba15-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4ba15-120">-Name</span></span>
<span data-ttu-id="4ba15-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4ba15-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba15-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ba15-122">-PassThru</span></span>
<span data-ttu-id="4ba15-123">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="4ba15-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4ba15-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba15-124">-ResourceId</span></span>
<span data-ttu-id="4ba15-125">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="4ba15-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba15-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ba15-126">-Confirm</span></span>
<span data-ttu-id="4ba15-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ba15-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba15-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba15-128">-WhatIf</span></span>
<span data-ttu-id="4ba15-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ba15-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba15-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ba15-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba15-131">CommonParameters</span></span>
<span data-ttu-id="4ba15-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba15-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ba15-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba15-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ba15-134">INPUTS</span></span>

### <span data-ttu-id="4ba15-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ba15-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="4ba15-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4ba15-136">System.String</span></span>

## <span data-ttu-id="4ba15-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ba15-137">OUTPUTS</span></span>

### <span data-ttu-id="4ba15-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ba15-138">System.Boolean</span></span>

## <span data-ttu-id="4ba15-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ba15-139">NOTES</span></span>

## <span data-ttu-id="4ba15-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ba15-140">RELATED LINKS</span></span>
