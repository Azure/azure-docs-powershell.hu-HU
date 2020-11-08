---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016247"
---
# <span data-ttu-id="397a5-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="397a5-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="397a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="397a5-102">SYNOPSIS</span></span>
<span data-ttu-id="397a5-103">Azonnal naplóz egy Azure RemoteApp-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="397a5-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="397a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="397a5-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="397a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="397a5-105">DESCRIPTION</span></span>
<span data-ttu-id="397a5-106">A **meghívó-AzureRemoteAppSessionLogoff** parancsmag azonnal kijelentkezik egy felhasználót az Azure remoteappben futó távoli munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="397a5-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="397a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="397a5-107">EXAMPLES</span></span>

### <span data-ttu-id="397a5-108">1. példa: felhasználó kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="397a5-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="397a5-109">A parancs kijelentkezik a felhasználóról, akinek az UPN-je van PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="397a5-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="397a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="397a5-110">PARAMETERS</span></span>

### <span data-ttu-id="397a5-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="397a5-111">-CollectionName</span></span>
<span data-ttu-id="397a5-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="397a5-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="397a5-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="397a5-113">-Profile</span></span>
<span data-ttu-id="397a5-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="397a5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="397a5-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="397a5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="397a5-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="397a5-116">-UserUpn</span></span>
<span data-ttu-id="397a5-117">Specifes egy felhasználó egyszerű felhasználónevét (UPN) adja meg PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="397a5-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="397a5-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="397a5-118">-Confirm</span></span>
<span data-ttu-id="397a5-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="397a5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="397a5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="397a5-120">-WhatIf</span></span>
<span data-ttu-id="397a5-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="397a5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="397a5-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="397a5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="397a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397a5-123">CommonParameters</span></span>
<span data-ttu-id="397a5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="397a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397a5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397a5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="397a5-126">INPUTS</span></span>

## <span data-ttu-id="397a5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="397a5-127">OUTPUTS</span></span>

## <span data-ttu-id="397a5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="397a5-128">NOTES</span></span>

## <span data-ttu-id="397a5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="397a5-129">RELATED LINKS</span></span>

[<span data-ttu-id="397a5-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="397a5-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="397a5-131">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="397a5-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="397a5-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="397a5-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


