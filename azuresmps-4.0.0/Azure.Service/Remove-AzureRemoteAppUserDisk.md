---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016147"
---
# <span data-ttu-id="d48b8-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="d48b8-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="d48b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d48b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d48b8-103">Egy felhasználó felhasználói lemezének eltávolítása Azure RemoteApp-gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="d48b8-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d48b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d48b8-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d48b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d48b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d48b8-106">A **Remove-AzureRemoteAppUserDisk** parancsmag eltávolítja egy felhasználó felhasználói lemezét egy Azure RemoteApp-gyűjteményből.</span><span class="sxs-lookup"><span data-stu-id="d48b8-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d48b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d48b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d48b8-108">1. példa: felhasználó lemezének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d48b8-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="d48b8-109">Ez a parancs eltávolítja egy olyan Azure Active Directory-felhasználó merevlemezét, aki az egyszerű felhasználónév a PattiFuller@contoso.com gyűjtemény Contoso01.</span><span class="sxs-lookup"><span data-stu-id="d48b8-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="d48b8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d48b8-110">PARAMETERS</span></span>

### <span data-ttu-id="d48b8-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d48b8-111">-CollectionName</span></span>
<span data-ttu-id="d48b8-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d48b8-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d48b8-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="d48b8-113">-Profile</span></span>
<span data-ttu-id="d48b8-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d48b8-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d48b8-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d48b8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d48b8-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d48b8-116">-UserUpn</span></span>
<span data-ttu-id="d48b8-117">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek a parancsmagja eltávolítja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="d48b8-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="d48b8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d48b8-118">-Confirm</span></span>
<span data-ttu-id="d48b8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d48b8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d48b8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d48b8-120">-WhatIf</span></span>
<span data-ttu-id="d48b8-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d48b8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d48b8-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d48b8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d48b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48b8-123">CommonParameters</span></span>
<span data-ttu-id="d48b8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d48b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48b8-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48b8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d48b8-126">INPUTS</span></span>

## <span data-ttu-id="d48b8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d48b8-127">OUTPUTS</span></span>

## <span data-ttu-id="d48b8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d48b8-128">NOTES</span></span>

## <span data-ttu-id="d48b8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d48b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="d48b8-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="d48b8-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


