---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491923"
---
# <span data-ttu-id="45de4-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="45de4-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="45de4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45de4-102">SYNOPSIS</span></span>
<span data-ttu-id="45de4-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="45de4-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45de4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45de4-104">SYNTAX</span></span>

### <span data-ttu-id="45de4-105">NamespaceCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45de4-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45de4-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="45de4-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45de4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45de4-107">DESCRIPTION</span></span>
<span data-ttu-id="45de4-108">A **teszt-AzureRmEventhubName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="45de4-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="45de4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="45de4-109">EXAMPLES</span></span>

### <span data-ttu-id="45de4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45de4-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="45de4-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül, ha elérhető.</span><span class="sxs-lookup"><span data-stu-id="45de4-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="45de4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="45de4-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="45de4-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="45de4-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="45de4-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="45de4-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="45de4-115">A "myAliasName" alias "MyNameSapceName" alias nevének elérhetőségi állapotát adja eredményül, ha az elérhető</span><span class="sxs-lookup"><span data-stu-id="45de4-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="45de4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45de4-116">PARAMETERS</span></span>

### <span data-ttu-id="45de4-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="45de4-117">-AliasName</span></span>
<span data-ttu-id="45de4-118">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="45de4-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="45de4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45de4-119">-DefaultProfile</span></span>
<span data-ttu-id="45de4-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45de4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45de4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="45de4-121">-Namespace</span></span>
<span data-ttu-id="45de4-122">Eventhub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="45de4-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="45de4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45de4-123">-ResourceGroupName</span></span>
<span data-ttu-id="45de4-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="45de4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="45de4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45de4-125">CommonParameters</span></span>
<span data-ttu-id="45de4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45de4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45de4-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45de4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45de4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45de4-128">INPUTS</span></span>

### <span data-ttu-id="45de4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45de4-129">System.String</span></span>

## <span data-ttu-id="45de4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45de4-130">OUTPUTS</span></span>

### <span data-ttu-id="45de4-131">Microsoft. Azure. Command. EventHub. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="45de4-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="45de4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45de4-132">NOTES</span></span>

## <span data-ttu-id="45de4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45de4-133">RELATED LINKS</span></span>
