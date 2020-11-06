---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495363"
---
# <span data-ttu-id="ad8ff-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="ad8ff-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="ad8ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8ff-103">A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)</span><span class="sxs-lookup"><span data-stu-id="ad8ff-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad8ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad8ff-104">SYNTAX</span></span>

### <span data-ttu-id="ad8ff-105">NamespaceCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad8ff-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad8ff-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad8ff-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad8ff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad8ff-107">DESCRIPTION</span></span>
<span data-ttu-id="ad8ff-108">A **teszt-AzureRmEventhubName** parancsmag a névtér nevének vagy aliasának elérhetőségét ellenőrzi (Dr. konfigurációs név).</span><span class="sxs-lookup"><span data-stu-id="ad8ff-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="ad8ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ad8ff-109">EXAMPLES</span></span>

### <span data-ttu-id="ad8ff-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad8ff-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="ad8ff-111">A "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ad8ff-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="ad8ff-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad8ff-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="ad8ff-113">Az "MyNameSapceName" névtér nevének elérhetőségi állapotát adja eredményül a következő okból: false (ok)</span><span class="sxs-lookup"><span data-stu-id="ad8ff-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="ad8ff-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="ad8ff-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="ad8ff-115">A "myAliasName" alias "MyNameSapceName" alias nevének elérhetőségi állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ad8ff-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="ad8ff-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad8ff-116">PARAMETERS</span></span>

### <span data-ttu-id="ad8ff-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="ad8ff-117">-AliasName</span></span>
<span data-ttu-id="ad8ff-118">DR konfigurációs név – alias neve</span><span class="sxs-lookup"><span data-stu-id="ad8ff-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8ff-119">-DefaultProfile</span></span>
<span data-ttu-id="ad8ff-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad8ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad8ff-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad8ff-121">-Namespace</span></span>
<span data-ttu-id="ad8ff-122">Eventhub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="ad8ff-122">Eventhub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad8ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad8ff-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ad8ff-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8ff-125">CommonParameters</span></span>
<span data-ttu-id="ad8ff-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad8ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad8ff-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad8ff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8ff-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad8ff-128">INPUTS</span></span>

### <span data-ttu-id="ad8ff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ad8ff-129">System.String</span></span>


## <span data-ttu-id="ad8ff-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad8ff-130">OUTPUTS</span></span>

### <span data-ttu-id="ad8ff-131">Microsoft. Azure. Command. EventHub. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="ad8ff-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="ad8ff-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad8ff-132">NOTES</span></span>

## <span data-ttu-id="ad8ff-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad8ff-133">RELATED LINKS</span></span>
