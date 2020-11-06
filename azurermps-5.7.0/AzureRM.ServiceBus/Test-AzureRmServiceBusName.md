---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494334"
---
# <span data-ttu-id="21a98-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="21a98-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="21a98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21a98-102">SYNOPSIS</span></span>
<span data-ttu-id="21a98-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="21a98-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21a98-104">SYNTAX</span></span>

### <span data-ttu-id="21a98-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="21a98-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a98-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="21a98-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21a98-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="21a98-107">DESCRIPTION</span></span>
<span data-ttu-id="21a98-108">A **teszt-AzureRmServiceBusName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="21a98-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="21a98-109">Példák</span><span class="sxs-lookup"><span data-stu-id="21a98-109">EXAMPLES</span></span>

### <span data-ttu-id="21a98-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21a98-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="21a98-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="21a98-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="21a98-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="21a98-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="21a98-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="21a98-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="21a98-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="21a98-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="21a98-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21a98-115">PARAMETERS</span></span>

### <span data-ttu-id="21a98-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="21a98-116">-AliasName</span></span>
<span data-ttu-id="21a98-117">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="21a98-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a98-118">-DefaultProfile</span></span>
<span data-ttu-id="21a98-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21a98-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a98-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21a98-120">-Namespace</span></span>
<span data-ttu-id="21a98-121">Servicebus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="21a98-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a98-122">-ResourceGroupName</span></span>
<span data-ttu-id="21a98-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="21a98-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a98-124">CommonParameters</span></span>
<span data-ttu-id="21a98-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21a98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21a98-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a98-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a98-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a98-127">INPUTS</span></span>

### <span data-ttu-id="21a98-128">System. String</span><span class="sxs-lookup"><span data-stu-id="21a98-128">System.String</span></span>


## <span data-ttu-id="21a98-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a98-129">OUTPUTS</span></span>

### <span data-ttu-id="21a98-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="21a98-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="21a98-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21a98-131">NOTES</span></span>

## <span data-ttu-id="21a98-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21a98-132">RELATED LINKS</span></span>
