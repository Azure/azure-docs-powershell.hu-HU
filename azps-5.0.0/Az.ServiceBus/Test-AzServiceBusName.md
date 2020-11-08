---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195322"
---
# <span data-ttu-id="fbbe9-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="fbbe9-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="fbbe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbe9-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="fbbe9-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="fbbe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbbe9-104">SYNTAX</span></span>

### <span data-ttu-id="fbbe9-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fbbe9-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbbe9-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fbbe9-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbe9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbbe9-107">DESCRIPTION</span></span>
<span data-ttu-id="fbbe9-108">A **teszt-AzServiceBusName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="fbbe9-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="fbbe9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fbbe9-109">EXAMPLES</span></span>

### <span data-ttu-id="fbbe9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbbe9-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="fbbe9-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="fbbe9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fbbe9-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="fbbe9-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="fbbe9-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="fbbe9-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="fbbe9-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="fbbe9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbbe9-115">PARAMETERS</span></span>

### <span data-ttu-id="fbbe9-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fbbe9-116">-AliasName</span></span>
<span data-ttu-id="fbbe9-117">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="fbbe9-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="fbbe9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbe9-118">-DefaultProfile</span></span>
<span data-ttu-id="fbbe9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbe9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fbbe9-120">-Namespace</span></span>
<span data-ttu-id="fbbe9-121">Servicebus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="fbbe9-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="fbbe9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbe9-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbbe9-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fbbe9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fbbe9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbe9-124">CommonParameters</span></span>
<span data-ttu-id="fbbe9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbbe9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbe9-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbe9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbe9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbbe9-127">INPUTS</span></span>

### <span data-ttu-id="fbbe9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fbbe9-128">System.String</span></span>

## <span data-ttu-id="fbbe9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbbe9-129">OUTPUTS</span></span>

### <span data-ttu-id="fbbe9-130">Microsoft. Azure. Command. ServiceBus. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="fbbe9-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="fbbe9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbbe9-131">NOTES</span></span>

## <span data-ttu-id="fbbe9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbbe9-132">RELATED LINKS</span></span>