---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: b78836a7d122dc05e4cd621b2d8994bd55697687
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669205"
---
# <span data-ttu-id="1567a-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1567a-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="1567a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1567a-102">SYNOPSIS</span></span>
<span data-ttu-id="1567a-103">A MigrationConfiguration lekérése a névtérhez</span><span class="sxs-lookup"><span data-stu-id="1567a-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="1567a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1567a-104">SYNTAX</span></span>

### <span data-ttu-id="1567a-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1567a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1567a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1567a-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1567a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1567a-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1567a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1567a-108">DESCRIPTION</span></span>
<span data-ttu-id="1567a-109">A **Get-AzServiceBusMigration** beolvassa a névtér áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="1567a-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="1567a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1567a-110">EXAMPLES</span></span>

### <span data-ttu-id="1567a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1567a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="1567a-112">Az "TestingNamespaceStandardMirgation" áttelepítési konfigurációs tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1567a-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="1567a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1567a-113">PARAMETERS</span></span>

### <span data-ttu-id="1567a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1567a-114">-DefaultProfile</span></span>
<span data-ttu-id="1567a-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1567a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1567a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1567a-116">-InputObject</span></span>
<span data-ttu-id="1567a-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="1567a-117">Namespace Object</span></span>

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

### <span data-ttu-id="1567a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1567a-118">-Name</span></span>
<span data-ttu-id="1567a-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="1567a-119">Namespace Name</span></span>

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

### <span data-ttu-id="1567a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1567a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1567a-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1567a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="1567a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1567a-122">-ResourceId</span></span>
<span data-ttu-id="1567a-123">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="1567a-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="1567a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1567a-124">CommonParameters</span></span>
<span data-ttu-id="1567a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1567a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1567a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1567a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1567a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1567a-127">INPUTS</span></span>

### <span data-ttu-id="1567a-128">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1567a-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="1567a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1567a-129">System.String</span></span>

## <span data-ttu-id="1567a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1567a-130">OUTPUTS</span></span>

### <span data-ttu-id="1567a-131">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1567a-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="1567a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1567a-132">NOTES</span></span>

## <span data-ttu-id="1567a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1567a-133">RELATED LINKS</span></span>
