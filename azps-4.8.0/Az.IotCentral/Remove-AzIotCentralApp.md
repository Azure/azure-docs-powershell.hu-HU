---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183566"
---
# <span data-ttu-id="5ac54-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5ac54-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="5ac54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ac54-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac54-103">Törli az IoT-os központi alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="5ac54-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="5ac54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ac54-104">SYNTAX</span></span>

### <span data-ttu-id="5ac54-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ac54-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac54-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac54-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac54-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac54-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac54-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ac54-108">DESCRIPTION</span></span>
<span data-ttu-id="5ac54-109">Törli a meglévő IoT-os központi alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="5ac54-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="5ac54-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5ac54-110">EXAMPLES</span></span>

### <span data-ttu-id="5ac54-111">Példa 1 delete és IoT Central alkalmazás</span><span class="sxs-lookup"><span data-stu-id="5ac54-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="5ac54-112">Törli a megadott IoT központi alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="5ac54-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="5ac54-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ac54-113">PARAMETERS</span></span>

### <span data-ttu-id="5ac54-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ac54-114">-AsJob</span></span>
<span data-ttu-id="5ac54-115">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="5ac54-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5ac54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac54-116">-DefaultProfile</span></span>
<span data-ttu-id="5ac54-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ac54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac54-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac54-118">-InputObject</span></span>
<span data-ttu-id="5ac54-119">IOT központi alkalmazás bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="5ac54-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac54-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ac54-120">-Name</span></span>
<span data-ttu-id="5ac54-121">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5ac54-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac54-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ac54-122">-PassThru</span></span>
<span data-ttu-id="5ac54-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ac54-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ac54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac54-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ac54-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ac54-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac54-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac54-126">-ResourceId</span></span>
<span data-ttu-id="5ac54-127">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="5ac54-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac54-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ac54-128">-Confirm</span></span>
<span data-ttu-id="5ac54-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ac54-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac54-130">-WhatIf</span></span>
<span data-ttu-id="5ac54-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ac54-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac54-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac54-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac54-133">CommonParameters</span></span>
<span data-ttu-id="5ac54-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ac54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac54-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ac54-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac54-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac54-136">INPUTS</span></span>

### <span data-ttu-id="5ac54-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac54-137">System.String</span></span>

### <span data-ttu-id="5ac54-138">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5ac54-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5ac54-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac54-139">OUTPUTS</span></span>

### <span data-ttu-id="5ac54-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ac54-140">System.Boolean</span></span>

## <span data-ttu-id="5ac54-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ac54-141">NOTES</span></span>

## <span data-ttu-id="5ac54-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac54-142">RELATED LINKS</span></span>
