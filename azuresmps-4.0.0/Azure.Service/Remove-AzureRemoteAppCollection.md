---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015868"
---
# <span data-ttu-id="1b987-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1b987-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="1b987-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b987-102">SYNOPSIS</span></span>
<span data-ttu-id="1b987-103">Azure RemoteApp-gyűjtemény eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1b987-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1b987-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b987-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b987-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b987-105">DESCRIPTION</span></span>
<span data-ttu-id="1b987-106">A **Remove-AzureRemoteAppCollection** parancsmag eltávolítja az Azure RemoteApp-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="1b987-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1b987-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1b987-107">EXAMPLES</span></span>

## <span data-ttu-id="1b987-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b987-108">PARAMETERS</span></span>

### <span data-ttu-id="1b987-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1b987-109">-CollectionName</span></span>
<span data-ttu-id="1b987-110">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b987-110">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1b987-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="1b987-111">-Profile</span></span>
<span data-ttu-id="1b987-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1b987-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b987-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1b987-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b987-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b987-114">-Confirm</span></span>
<span data-ttu-id="1b987-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b987-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b987-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b987-116">-WhatIf</span></span>
<span data-ttu-id="1b987-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b987-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b987-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b987-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b987-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b987-119">CommonParameters</span></span>
<span data-ttu-id="1b987-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b987-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b987-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b987-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b987-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b987-122">INPUTS</span></span>

## <span data-ttu-id="1b987-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b987-123">OUTPUTS</span></span>

## <span data-ttu-id="1b987-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b987-124">NOTES</span></span>

## <span data-ttu-id="1b987-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b987-125">RELATED LINKS</span></span>

[<span data-ttu-id="1b987-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1b987-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="1b987-127">Új – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1b987-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="1b987-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1b987-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="1b987-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1b987-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


