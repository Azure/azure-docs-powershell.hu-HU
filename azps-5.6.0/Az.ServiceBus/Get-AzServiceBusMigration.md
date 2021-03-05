---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 29595722be5f7659d63828462ade0826ac85e610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005637"
---
# <span data-ttu-id="2f441-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2f441-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="2f441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f441-102">SYNOPSIS</span></span>
<span data-ttu-id="2f441-103">Beolvassa a MigrationConfiguration nevet a névtérhez</span><span class="sxs-lookup"><span data-stu-id="2f441-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="2f441-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f441-104">SYNTAX</span></span>

### <span data-ttu-id="2f441-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f441-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f441-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f441-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f441-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f441-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f441-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f441-108">DESCRIPTION</span></span>
<span data-ttu-id="2f441-109">A **Get-AzServiceBusMigration** lekéri a névtér áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="2f441-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="2f441-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f441-110">EXAMPLES</span></span>

### <span data-ttu-id="2f441-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2f441-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="2f441-112">A "TestingNamespaceStandardMigration" áttelepítési konfigurációs tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f441-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="2f441-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f441-113">PARAMETERS</span></span>

### <span data-ttu-id="2f441-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f441-114">-DefaultProfile</span></span>
<span data-ttu-id="2f441-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f441-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f441-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f441-116">-InputObject</span></span>
<span data-ttu-id="2f441-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="2f441-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f441-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2f441-118">-Name</span></span>
<span data-ttu-id="2f441-119">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2f441-119">Namespace Name</span></span>

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

### <span data-ttu-id="2f441-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f441-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f441-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2f441-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2f441-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f441-122">-ResourceId</span></span>
<span data-ttu-id="2f441-123">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="2f441-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f441-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f441-124">CommonParameters</span></span>
<span data-ttu-id="2f441-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f441-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f441-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f441-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f441-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f441-127">INPUTS</span></span>

### <span data-ttu-id="2f441-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2f441-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="2f441-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2f441-129">System.String</span></span>

## <span data-ttu-id="2f441-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f441-130">OUTPUTS</span></span>

### <span data-ttu-id="2f441-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2f441-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="2f441-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f441-132">NOTES</span></span>

## <span data-ttu-id="2f441-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f441-133">RELATED LINKS</span></span>
