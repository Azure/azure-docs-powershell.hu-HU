---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491324"
---
# <span data-ttu-id="e5dd5-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd5-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="e5dd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dd5-103">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="e5dd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5dd5-104">SYNTAX</span></span>

### <span data-ttu-id="e5dd5-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd5-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="e5dd5-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="e5dd5-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="e5dd5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5dd5-107">DESCRIPTION</span></span>
<span data-ttu-id="e5dd5-108">A Select-AzureRmProfile parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="e5dd5-109">Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="e5dd5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e5dd5-110">EXAMPLES</span></span>

### <span data-ttu-id="e5dd5-111">1. példa: profil kijelölése PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd5-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e5dd5-112">Ez a példa kijelöl egy profilt egy olyan PSAzureProfile, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="e5dd5-113">2. példa: profil kiválasztása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="e5dd5-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e5dd5-114">Ebben a példában egy JSON-fájlból kiválaszt egy profilt, amelyet a parancsmagnak továbbítanak.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="e5dd5-115">Ezt a JSON-fájlt a Save-AzureRmProfile hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="e5dd5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5dd5-116">PARAMETERS</span></span>

### <span data-ttu-id="e5dd5-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e5dd5-117">-Path</span></span>
<span data-ttu-id="e5dd5-118">A Save-AzureRMProfile használatával mentett profil-információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dd5-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5dd5-119">-Profile</span></span>
<span data-ttu-id="e5dd5-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5dd5-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e5dd5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dd5-122">CommonParameters</span></span>
<span data-ttu-id="e5dd5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5dd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dd5-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5dd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dd5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5dd5-125">INPUTS</span></span>

## <span data-ttu-id="e5dd5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5dd5-126">OUTPUTS</span></span>

### <span data-ttu-id="e5dd5-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd5-127">PSAzureProfile</span></span>

## <span data-ttu-id="e5dd5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5dd5-128">NOTES</span></span>

## <span data-ttu-id="e5dd5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5dd5-129">RELATED LINKS</span></span>

[<span data-ttu-id="e5dd5-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="e5dd5-130">Get-AzureRMContext</span></span>]()

