---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015737"
---
# <span data-ttu-id="e4f9b-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e4f9b-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="e4f9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f9b-103">Az Azure RemoteApp-gyűjtemény frissítése egy új sablon képével.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="e4f9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4f9b-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f9b-106">Az **Update-AzureRemoteAppCollection** parancsmag az Azure RemoteApp Collectiont egy új sablon képével frissíti.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="e4f9b-107">Miután a frissítés befejeződött, a meglévő munkameneteket használóknak egy óra elteltével ki kell jelentkeznie, mielőtt automatikusan kijelentkezett. A bejelentkezéskor az újonnan frissített gyűjteményhez csatlakoznak.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="e4f9b-108">Ha azt szeretné, hogy a felhasználók azonnal jelentkezzenek ki, amint a gyűjtemény frissítve van, adja meg a *ForceLogoffWhenUpdateComplete* paramétert.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="e4f9b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e4f9b-109">EXAMPLES</span></span>

## <span data-ttu-id="e4f9b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4f9b-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f9b-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e4f9b-111">-CollectionName</span></span>
<span data-ttu-id="e4f9b-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="e4f9b-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="e4f9b-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="e4f9b-114">Azt jelzi, hogy a parancsmag a frissítés befejeződése után azonnal aláírja a felhasználókat a meglévő munkamenetekről.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="e4f9b-115">Amikor a felhasználók ismét bejelentkeznek, csatlakoznak az újonnan frissített gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="e4f9b-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e4f9b-116">-ImageName</span></span>
<span data-ttu-id="e4f9b-117">Egy Azure RemoteApp-sablon nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="e4f9b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="e4f9b-118">-Profile</span></span>
<span data-ttu-id="e4f9b-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4f9b-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4f9b-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e4f9b-121">-SubnetName</span></span>
<span data-ttu-id="e4f9b-122">Annak az alhálózatnak a neve, amelybe a gyűjteményt át szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f9b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4f9b-123">-Confirm</span></span>
<span data-ttu-id="e4f9b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f9b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f9b-125">-WhatIf</span></span>
<span data-ttu-id="e4f9b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f9b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f9b-128">CommonParameters</span></span>
<span data-ttu-id="e4f9b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4f9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f9b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f9b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f9b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4f9b-131">INPUTS</span></span>

## <span data-ttu-id="e4f9b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4f9b-132">OUTPUTS</span></span>

## <span data-ttu-id="e4f9b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4f9b-133">NOTES</span></span>

## <span data-ttu-id="e4f9b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4f9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4f9b-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e4f9b-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="e4f9b-136">Új – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e4f9b-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="e4f9b-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e4f9b-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


