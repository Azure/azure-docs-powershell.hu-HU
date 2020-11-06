---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497335"
---
# <span data-ttu-id="87df9-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="87df9-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="87df9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87df9-102">SYNOPSIS</span></span>
<span data-ttu-id="87df9-103">A MigrationConfiguration lekérése a névtérhez</span><span class="sxs-lookup"><span data-stu-id="87df9-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87df9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87df9-104">SYNTAX</span></span>

### <span data-ttu-id="87df9-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87df9-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87df9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87df9-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87df9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87df9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87df9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87df9-108">DESCRIPTION</span></span>
<span data-ttu-id="87df9-109">A **Get-AzureRmServiceBusMigration** beolvassa a névtér áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="87df9-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="87df9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87df9-110">EXAMPLES</span></span>

### <span data-ttu-id="87df9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="87df9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="87df9-112">Az "TestingNamespaceStandardMirgation" áttelepítési konfigurációs tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87df9-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="87df9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87df9-113">PARAMETERS</span></span>

### <span data-ttu-id="87df9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87df9-114">-DefaultProfile</span></span>
<span data-ttu-id="87df9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87df9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87df9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87df9-116">-InputObject</span></span>
<span data-ttu-id="87df9-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="87df9-117">Namespace Object</span></span>

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

### <span data-ttu-id="87df9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87df9-118">-Name</span></span>
<span data-ttu-id="87df9-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="87df9-119">Namespace Name</span></span>

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

### <span data-ttu-id="87df9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87df9-120">-ResourceGroupName</span></span>
<span data-ttu-id="87df9-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="87df9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="87df9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87df9-122">-ResourceId</span></span>
<span data-ttu-id="87df9-123">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="87df9-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="87df9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87df9-124">CommonParameters</span></span>
<span data-ttu-id="87df9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87df9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87df9-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87df9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87df9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87df9-127">INPUTS</span></span>

### <span data-ttu-id="87df9-128">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="87df9-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="87df9-129">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87df9-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="87df9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="87df9-130">System.String</span></span>

## <span data-ttu-id="87df9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87df9-131">OUTPUTS</span></span>

### <span data-ttu-id="87df9-132">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="87df9-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="87df9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87df9-133">NOTES</span></span>

## <span data-ttu-id="87df9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87df9-134">RELATED LINKS</span></span>
