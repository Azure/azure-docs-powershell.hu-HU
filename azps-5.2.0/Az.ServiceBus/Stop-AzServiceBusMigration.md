---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369066"
---
# <span data-ttu-id="0053c-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0053c-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="0053c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0053c-102">SYNOPSIS</span></span>
<span data-ttu-id="0053c-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="0053c-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="0053c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0053c-104">SYNTAX</span></span>

### <span data-ttu-id="0053c-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0053c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0053c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0053c-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0053c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0053c-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0053c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0053c-108">DESCRIPTION</span></span>
<span data-ttu-id="0053c-109">A **Stop-AzServiceBusMigration** parancsmagok megszakítják az áttelepítést a Standard és a prémium névtér között</span><span class="sxs-lookup"><span data-stu-id="0053c-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="0053c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0053c-110">EXAMPLES</span></span>

### <span data-ttu-id="0053c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0053c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="0053c-112">A parancsmag megszakítja az áttelepítési konfiguráció létrehozásakor a Standard és a Premium névtér közötti áttelepítést.</span><span class="sxs-lookup"><span data-stu-id="0053c-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="0053c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0053c-113">PARAMETERS</span></span>

### <span data-ttu-id="0053c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0053c-114">-DefaultProfile</span></span>
<span data-ttu-id="0053c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0053c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0053c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0053c-116">-InputObject</span></span>
<span data-ttu-id="0053c-117">Service Bus Migration Configuration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="0053c-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="0053c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0053c-118">-Name</span></span>
<span data-ttu-id="0053c-119">Normál névtérnév</span><span class="sxs-lookup"><span data-stu-id="0053c-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="0053c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0053c-120">-PassThru</span></span>
<span data-ttu-id="0053c-121">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="0053c-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0053c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0053c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0053c-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0053c-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0053c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0053c-124">-ResourceId</span></span>
<span data-ttu-id="0053c-125">Service Bus Migration Configuration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="0053c-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="0053c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0053c-126">-Confirm</span></span>
<span data-ttu-id="0053c-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0053c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0053c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0053c-128">-WhatIf</span></span>
<span data-ttu-id="0053c-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0053c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0053c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0053c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0053c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0053c-131">CommonParameters</span></span>
<span data-ttu-id="0053c-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0053c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0053c-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0053c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0053c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0053c-134">INPUTS</span></span>

### <span data-ttu-id="0053c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0053c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="0053c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0053c-136">System.String</span></span>

## <span data-ttu-id="0053c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0053c-137">OUTPUTS</span></span>

### <span data-ttu-id="0053c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0053c-138">System.Boolean</span></span>

## <span data-ttu-id="0053c-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0053c-139">NOTES</span></span>

## <span data-ttu-id="0053c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0053c-140">RELATED LINKS</span></span>
