---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015698"
---
# <span data-ttu-id="43a2d-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="43a2d-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="43a2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="43a2d-103">Egy felhasználó merevlemezét átmásolja egyik Azure RemoteApp-gyűjteményből a másikba.</span><span class="sxs-lookup"><span data-stu-id="43a2d-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="43a2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43a2d-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43a2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="43a2d-106">A **copy-AzureRemoteAppUserDisk** parancsmag egy felhasználó felhasználói lemezét egy Azure RemoteApp-gyűjteményből egy másikba másolja át.</span><span class="sxs-lookup"><span data-stu-id="43a2d-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="43a2d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="43a2d-108">Példa 1: felhasználó lemezének másolása</span><span class="sxs-lookup"><span data-stu-id="43a2d-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="43a2d-109">A parancs átmásolja egy Azure Active Directory-felhasználó felhasználói lemezét, aki az egyszerű felhasználónév a gyűjtemény PattiFuller@contoso.com Contoso01 a gyűjtemény Contoso02.</span><span class="sxs-lookup"><span data-stu-id="43a2d-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="43a2d-110">Ha a PattiFuller@contoso.com Contoso02 már létezik egy felhasználói lemez, a parancs felülírja.</span><span class="sxs-lookup"><span data-stu-id="43a2d-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="43a2d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43a2d-111">PARAMETERS</span></span>

### <span data-ttu-id="43a2d-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="43a2d-112">-DestinationCollectionName</span></span>
<span data-ttu-id="43a2d-113">A cél Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43a2d-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a2d-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="43a2d-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="43a2d-115">Azt jelzi, hogy ez a parancsmag felülír egy meglévő felhasználói merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="43a2d-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="43a2d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="43a2d-116">-Profile</span></span>
<span data-ttu-id="43a2d-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="43a2d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43a2d-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="43a2d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43a2d-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="43a2d-119">-SourceCollectionName</span></span>
<span data-ttu-id="43a2d-120">A forrás Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43a2d-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a2d-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="43a2d-121">-UserUpn</span></span>
<span data-ttu-id="43a2d-122">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek a parancsmagja a lemezt másolja.</span><span class="sxs-lookup"><span data-stu-id="43a2d-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a2d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a2d-123">CommonParameters</span></span>
<span data-ttu-id="43a2d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43a2d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a2d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a2d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a2d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a2d-126">INPUTS</span></span>

## <span data-ttu-id="43a2d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a2d-127">OUTPUTS</span></span>

## <span data-ttu-id="43a2d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43a2d-128">NOTES</span></span>

## <span data-ttu-id="43a2d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43a2d-129">RELATED LINKS</span></span>

[<span data-ttu-id="43a2d-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="43a2d-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


