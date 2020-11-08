---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015632"
---
# <span data-ttu-id="959d2-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="959d2-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="959d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="959d2-102">SYNOPSIS</span></span>
<span data-ttu-id="959d2-103">Beolvassa az Azure RemoteApp-gyűjtemény használati adatait.</span><span class="sxs-lookup"><span data-stu-id="959d2-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="959d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="959d2-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="959d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="959d2-105">DESCRIPTION</span></span>
<span data-ttu-id="959d2-106">A **Get-AzureRemoteAppCollectionUsageDetails** parancsmag beolvassa az Azure RemoteApp-gyűjtemény használati adatait.</span><span class="sxs-lookup"><span data-stu-id="959d2-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="959d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="959d2-107">EXAMPLES</span></span>

### <span data-ttu-id="959d2-108">Példa 1: egy gyűjtemény használati adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="959d2-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="959d2-109">Ez a parancs a 2014-as év december hónapjában a contoso nevű Azure RemoteApp-gyűjtemény használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="959d2-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="959d2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="959d2-110">PARAMETERS</span></span>

### <span data-ttu-id="959d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="959d2-111">-AsJob</span></span>
<span data-ttu-id="959d2-112">Azt jelzi, hogy a parancsmag a háttérben fut Windows PowerShell-feladatként.</span><span class="sxs-lookup"><span data-stu-id="959d2-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="959d2-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="959d2-113">-CollectionName</span></span>
<span data-ttu-id="959d2-114">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="959d2-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="959d2-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="959d2-115">-Profile</span></span>
<span data-ttu-id="959d2-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="959d2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="959d2-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="959d2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="959d2-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="959d2-118">-UsageMonth</span></span>
<span data-ttu-id="959d2-119">Annak a hónapnak a két számjegyből álló számát adja meg, amelynek a használati adatait meg szeretné kapni.</span><span class="sxs-lookup"><span data-stu-id="959d2-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="959d2-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="959d2-120">-UsageYear</span></span>
<span data-ttu-id="959d2-121">Azt a négy jegyű évet adja meg, amelyre a használati adatok beszerzése szükséges.</span><span class="sxs-lookup"><span data-stu-id="959d2-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="959d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="959d2-122">CommonParameters</span></span>
<span data-ttu-id="959d2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="959d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="959d2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="959d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="959d2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="959d2-125">INPUTS</span></span>

## <span data-ttu-id="959d2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="959d2-126">OUTPUTS</span></span>

## <span data-ttu-id="959d2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="959d2-127">NOTES</span></span>

## <span data-ttu-id="959d2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="959d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="959d2-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="959d2-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="959d2-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="959d2-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


