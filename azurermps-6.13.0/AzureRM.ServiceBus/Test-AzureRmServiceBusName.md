---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494905"
---
# <span data-ttu-id="687ff-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="687ff-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="687ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="687ff-102">SYNOPSIS</span></span>
<span data-ttu-id="687ff-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="687ff-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="687ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="687ff-104">SYNTAX</span></span>

### <span data-ttu-id="687ff-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="687ff-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="687ff-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="687ff-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="687ff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="687ff-107">DESCRIPTION</span></span>
<span data-ttu-id="687ff-108">A **teszt-AzureRmServiceBusName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="687ff-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="687ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="687ff-109">EXAMPLES</span></span>

### <span data-ttu-id="687ff-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="687ff-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="687ff-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="687ff-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="687ff-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="687ff-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="687ff-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="687ff-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="687ff-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="687ff-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="687ff-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="687ff-115">PARAMETERS</span></span>

### <span data-ttu-id="687ff-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="687ff-116">-AliasName</span></span>
<span data-ttu-id="687ff-117">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="687ff-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687ff-118">-DefaultProfile</span></span>
<span data-ttu-id="687ff-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="687ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687ff-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="687ff-120">-Namespace</span></span>
<span data-ttu-id="687ff-121">Servicebus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="687ff-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="687ff-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="687ff-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687ff-124">CommonParameters</span></span>
<span data-ttu-id="687ff-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="687ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687ff-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="687ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687ff-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="687ff-127">INPUTS</span></span>

### <span data-ttu-id="687ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="687ff-128">System.String</span></span>

## <span data-ttu-id="687ff-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="687ff-129">OUTPUTS</span></span>

### <span data-ttu-id="687ff-130">Microsoft. Azure. Command. ServiceBus. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="687ff-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="687ff-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="687ff-131">NOTES</span></span>

## <span data-ttu-id="687ff-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="687ff-132">RELATED LINKS</span></span>
