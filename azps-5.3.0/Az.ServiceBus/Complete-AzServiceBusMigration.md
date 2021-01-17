---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479680"
---
# <span data-ttu-id="7f870-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="7f870-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="7f870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f870-102">SYNOPSIS</span></span>
<span data-ttu-id="7f870-103">A parancsmagok az Áttelepítés standardról prémium névtérre teljesként, a normál névtér kapcsolati karakterláncai pedig a Prémium névtérre mutatnak</span><span class="sxs-lookup"><span data-stu-id="7f870-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7f870-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f870-104">SYNTAX</span></span>

### <span data-ttu-id="7f870-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f870-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f870-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f870-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f870-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f870-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f870-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f870-108">DESCRIPTION</span></span>
<span data-ttu-id="7f870-109">A **Complete-AzServiceBusMigration** parancsmagok az Áttelepítés standardról prémium névtérre teljesként vannak beállítva, és a normál névtér kapcsolati karakterláncai mostantól a Prémium névtérre mutatnak</span><span class="sxs-lookup"><span data-stu-id="7f870-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7f870-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f870-110">EXAMPLES</span></span>

### <span data-ttu-id="7f870-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7f870-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="7f870-112">A "NamespaceStandardMigration" névtér áttelepítését befejezettként állítja be.</span><span class="sxs-lookup"><span data-stu-id="7f870-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="7f870-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f870-113">PARAMETERS</span></span>

### <span data-ttu-id="7f870-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f870-114">-DefaultProfile</span></span>
<span data-ttu-id="7f870-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f870-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f870-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f870-116">-InputObject</span></span>
<span data-ttu-id="7f870-117">Service Bus Migration configuration - Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="7f870-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f870-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7f870-118">-Name</span></span>
<span data-ttu-id="7f870-119">Normál névtérnév</span><span class="sxs-lookup"><span data-stu-id="7f870-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f870-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f870-120">-PassThru</span></span>
<span data-ttu-id="7f870-121">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="7f870-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7f870-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f870-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f870-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7f870-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f870-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f870-124">-ResourceId</span></span>
<span data-ttu-id="7f870-125">Service Bus Migration - Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="7f870-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f870-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f870-126">-Confirm</span></span>
<span data-ttu-id="7f870-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7f870-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f870-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f870-128">-WhatIf</span></span>
<span data-ttu-id="7f870-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7f870-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f870-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f870-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f870-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f870-131">CommonParameters</span></span>
<span data-ttu-id="7f870-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f870-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f870-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f870-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f870-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f870-134">INPUTS</span></span>

### <span data-ttu-id="7f870-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7f870-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="7f870-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7f870-136">System.String</span></span>

## <span data-ttu-id="7f870-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f870-137">OUTPUTS</span></span>

### <span data-ttu-id="7f870-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f870-138">System.Boolean</span></span>

## <span data-ttu-id="7f870-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f870-139">NOTES</span></span>

## <span data-ttu-id="7f870-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f870-140">RELATED LINKS</span></span>
