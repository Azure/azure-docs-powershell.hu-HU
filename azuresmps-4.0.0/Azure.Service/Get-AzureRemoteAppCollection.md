---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016329"
---
# <span data-ttu-id="d4613-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d4613-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="d4613-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4613-102">SYNOPSIS</span></span>
<span data-ttu-id="d4613-103">Beolvassa az Azure RemoteApp-gyűjtemény adatait.</span><span class="sxs-lookup"><span data-stu-id="d4613-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d4613-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4613-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4613-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4613-105">DESCRIPTION</span></span>
<span data-ttu-id="d4613-106">A **Get-AzureRemoteAppCollection** parancsmag információkat keres az Azure RemoteApp-gyűjteményekről a Microsoft Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d4613-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="d4613-107">Egy olyan objektumot ad eredményül, amely egy adott gyűjtemény adataival rendelkezik, vagy ha nem ad meg gyűjteményt, az aktuális előfizetéshez tartozó összes gyűjtemény esetében.</span><span class="sxs-lookup"><span data-stu-id="d4613-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="d4613-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d4613-108">EXAMPLES</span></span>

### <span data-ttu-id="d4613-109">Példa 1: az összes gyűjtemény listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4613-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="d4613-110">Ez a parancs az összes Azure RemoteApp-gyűjtemény listáját visszaküldi az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d4613-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="d4613-111">2. példa: információk kérése egy adott gyűjteményről</span><span class="sxs-lookup"><span data-stu-id="d4613-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="d4613-112">Ez a parancs információt ad a ContosoApps nevű Azure RemoteApp-gyűjteményről.</span><span class="sxs-lookup"><span data-stu-id="d4613-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="d4613-113">3. példa: gyűjtemények listájának beszerzése helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="d4613-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="d4613-114">Ez a parancs az összes Azure RemoteApp-gyűjtemény listáját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="d4613-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="d4613-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4613-115">PARAMETERS</span></span>

### <span data-ttu-id="d4613-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d4613-116">-CollectionName</span></span>
<span data-ttu-id="d4613-117">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4613-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d4613-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4613-118">-Profile</span></span>
<span data-ttu-id="d4613-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d4613-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4613-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d4613-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4613-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4613-121">CommonParameters</span></span>
<span data-ttu-id="d4613-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4613-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4613-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4613-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4613-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4613-124">INPUTS</span></span>

## <span data-ttu-id="d4613-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4613-125">OUTPUTS</span></span>

## <span data-ttu-id="d4613-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4613-126">NOTES</span></span>

## <span data-ttu-id="d4613-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4613-127">RELATED LINKS</span></span>

[<span data-ttu-id="d4613-128">Új – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d4613-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="d4613-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d4613-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="d4613-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d4613-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="d4613-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d4613-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


