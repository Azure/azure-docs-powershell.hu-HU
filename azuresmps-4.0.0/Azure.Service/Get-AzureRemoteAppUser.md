---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016316"
---
# <span data-ttu-id="8e7ff-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8e7ff-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="8e7ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7ff-103">Felsorolja az Azure RemoteApp-gyűjtemény felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8e7ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e7ff-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e7ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7ff-106">A **Get-AzureRemoteAppUser** parancsmag felsorolja az Azure RemoteApp-gyűjtemény felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8e7ff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e7ff-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7ff-108">Példa 1: egy gyűjtemény felhasználóinak listázása</span><span class="sxs-lookup"><span data-stu-id="8e7ff-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="8e7ff-109">Ez a parancs felsorolja azokat a felhasználókat, akik hozzáféréssel rendelkeznek az Azure RemoteApp-gyűjteményhez a contoso nevű gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="8e7ff-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e7ff-110">PARAMETERS</span></span>

### <span data-ttu-id="8e7ff-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="8e7ff-111">-Alias</span></span>
<span data-ttu-id="8e7ff-112">Egy közzétett program-aliast ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-112">Specifies a published program alias.</span></span>
<span data-ttu-id="8e7ff-113">Ezt a paramétert csak a per-app közzétételi módjában tudja használni.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-113">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ff-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8e7ff-114">-CollectionName</span></span>
<span data-ttu-id="8e7ff-115">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="8e7ff-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="8e7ff-116">-Profile</span></span>
<span data-ttu-id="8e7ff-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e7ff-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e7ff-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="8e7ff-119">-UserUpn</span></span>
<span data-ttu-id="8e7ff-120">Annak a felhasználónak az egyszerű felhasználónevét adja meg, amelynek a listáját információkat listázhatja.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="8e7ff-121">Például: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8e7ff-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8e7ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7ff-122">CommonParameters</span></span>
<span data-ttu-id="8e7ff-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e7ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7ff-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7ff-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e7ff-125">INPUTS</span></span>

## <span data-ttu-id="8e7ff-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e7ff-126">OUTPUTS</span></span>

## <span data-ttu-id="8e7ff-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-127">NOTES</span></span>

## <span data-ttu-id="8e7ff-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e7ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e7ff-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8e7ff-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="8e7ff-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="8e7ff-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="8e7ff-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8e7ff-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


