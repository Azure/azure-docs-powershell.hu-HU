---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025347"
---
# <span data-ttu-id="4f818-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="4f818-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="4f818-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f818-102">SYNOPSIS</span></span>
<span data-ttu-id="4f818-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="4f818-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4f818-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f818-104">SYNTAX</span></span>

### <span data-ttu-id="4f818-105">NamespaceCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f818-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f818-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4f818-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f818-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f818-107">DESCRIPTION</span></span>
<span data-ttu-id="4f818-108">A **teszt-AzEventhubName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="4f818-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4f818-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4f818-109">EXAMPLES</span></span>

### <span data-ttu-id="4f818-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4f818-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="4f818-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül, ha elérhető.</span><span class="sxs-lookup"><span data-stu-id="4f818-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="4f818-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4f818-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="4f818-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="4f818-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="4f818-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="4f818-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="4f818-115">A "myAliasName" alias "MyNameSapceName" alias nevének elérhetőségi állapotát adja eredményül, ha az elérhető</span><span class="sxs-lookup"><span data-stu-id="4f818-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="4f818-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f818-116">PARAMETERS</span></span>

### <span data-ttu-id="4f818-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4f818-117">-AliasName</span></span>
<span data-ttu-id="4f818-118">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="4f818-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="4f818-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f818-119">-DefaultProfile</span></span>
<span data-ttu-id="4f818-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f818-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f818-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4f818-121">-Namespace</span></span>
<span data-ttu-id="4f818-122">Eventhub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="4f818-122">Eventhub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f818-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f818-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f818-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4f818-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f818-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f818-125">CommonParameters</span></span>
<span data-ttu-id="4f818-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f818-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f818-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f818-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f818-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f818-128">INPUTS</span></span>

### <span data-ttu-id="4f818-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4f818-129">System.String</span></span>

## <span data-ttu-id="4f818-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f818-130">OUTPUTS</span></span>

### <span data-ttu-id="4f818-131">Microsoft. Azure. Command. EventHub. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="4f818-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="4f818-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f818-132">NOTES</span></span>

## <span data-ttu-id="4f818-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f818-133">RELATED LINKS</span></span>
