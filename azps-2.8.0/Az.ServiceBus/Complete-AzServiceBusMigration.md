---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 0b8290a9cb782ee3801e34e55fef1997a4745aee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838062"
---
# <span data-ttu-id="c68ea-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c68ea-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="c68ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c68ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c68ea-103">Parancsmagok: a standard-ról prémium névtérre való áttelepítést teljesként és a standard névtér kapcsolati karakterláncait a prémium névtér pontra mutathatja.</span><span class="sxs-lookup"><span data-stu-id="c68ea-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="c68ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c68ea-104">SYNTAX</span></span>

### <span data-ttu-id="c68ea-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c68ea-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c68ea-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c68ea-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c68ea-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c68ea-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68ea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c68ea-108">DESCRIPTION</span></span>
<span data-ttu-id="c68ea-109">A **Complete-AzServiceBusMigration** parancsmagok a standard-ról prémium névtérre való áttelepítést teljes méretűvé és a standard névtér kapcsolati karakterláncait a prémium névtérre mutatják.</span><span class="sxs-lookup"><span data-stu-id="c68ea-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="c68ea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c68ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c68ea-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c68ea-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="c68ea-112">A "NamespaceStandardMigration" névtér áttelepítését állítja be befejezettként.</span><span class="sxs-lookup"><span data-stu-id="c68ea-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="c68ea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c68ea-113">PARAMETERS</span></span>

### <span data-ttu-id="c68ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68ea-114">-DefaultProfile</span></span>
<span data-ttu-id="c68ea-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c68ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68ea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c68ea-116">-InputObject</span></span>
<span data-ttu-id="c68ea-117">A szolgáltatás busz áttelepítésének konfigurációja – standard Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="c68ea-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="c68ea-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c68ea-118">-Name</span></span>
<span data-ttu-id="c68ea-119">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="c68ea-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="c68ea-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c68ea-120">-PassThru</span></span>
<span data-ttu-id="c68ea-121">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="c68ea-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c68ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="c68ea-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c68ea-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c68ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c68ea-124">-ResourceId</span></span>
<span data-ttu-id="c68ea-125">Szolgáltatás busz áttelepítése – normál névtér erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c68ea-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="c68ea-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c68ea-126">-Confirm</span></span>
<span data-ttu-id="c68ea-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c68ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68ea-128">-WhatIf</span></span>
<span data-ttu-id="c68ea-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c68ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68ea-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c68ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68ea-131">CommonParameters</span></span>
<span data-ttu-id="c68ea-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c68ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68ea-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68ea-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68ea-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c68ea-134">INPUTS</span></span>

### <span data-ttu-id="c68ea-135">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c68ea-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="c68ea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c68ea-136">System.String</span></span>

## <span data-ttu-id="c68ea-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c68ea-137">OUTPUTS</span></span>

### <span data-ttu-id="c68ea-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c68ea-138">System.Boolean</span></span>

## <span data-ttu-id="c68ea-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c68ea-139">NOTES</span></span>

## <span data-ttu-id="c68ea-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c68ea-140">RELATED LINKS</span></span>
