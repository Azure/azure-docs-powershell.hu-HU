---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016330"
---
# <span data-ttu-id="8415a-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="8415a-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="8415a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8415a-102">SYNOPSIS</span></span>
<span data-ttu-id="8415a-103">Beolvassa az Azure RemoteApp-gyűjtemény használati összegzését.</span><span class="sxs-lookup"><span data-stu-id="8415a-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8415a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8415a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8415a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8415a-105">DESCRIPTION</span></span>
<span data-ttu-id="8415a-106">A **Get-AzureRemoteAppCollectionUsageSummary** parancsmag az Azure RemoteApp-gyűjtemény használati összefoglalását keresi meg.</span><span class="sxs-lookup"><span data-stu-id="8415a-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8415a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8415a-107">EXAMPLES</span></span>

### <span data-ttu-id="8415a-108">Példa 1: használati összefoglalás beszerzése</span><span class="sxs-lookup"><span data-stu-id="8415a-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="8415a-109">Ez a parancs a 2014-as év december hónapjában a contoso nevű gyűjtemény használati összefoglalását kapja.</span><span class="sxs-lookup"><span data-stu-id="8415a-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="8415a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8415a-110">PARAMETERS</span></span>

### <span data-ttu-id="8415a-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8415a-111">-CollectionName</span></span>
<span data-ttu-id="8415a-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8415a-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8415a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="8415a-113">-Profile</span></span>
<span data-ttu-id="8415a-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8415a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8415a-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8415a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8415a-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="8415a-116">-UsageMonth</span></span>
<span data-ttu-id="8415a-117">Annak a hónapnak a kétjegyű számát adja meg, amelyhez a használati összegzést be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="8415a-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="8415a-118">Ha ez a paraméter nincs megadva, ez a parancsmag az aktuális hónap használati értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8415a-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8415a-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="8415a-119">-UsageYear</span></span>
<span data-ttu-id="8415a-120">Azt a négy jegyű évet adja meg, amelyhez a használati összegzést be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="8415a-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="8415a-121">Ha ez a paraméter nincs megadva, ez a parancsmag az aktuális év használati összegzését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8415a-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8415a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8415a-122">CommonParameters</span></span>
<span data-ttu-id="8415a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8415a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8415a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8415a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8415a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8415a-125">INPUTS</span></span>

## <span data-ttu-id="8415a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8415a-126">OUTPUTS</span></span>

## <span data-ttu-id="8415a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8415a-127">NOTES</span></span>

## <span data-ttu-id="8415a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8415a-128">RELATED LINKS</span></span>

[<span data-ttu-id="8415a-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8415a-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="8415a-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="8415a-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


