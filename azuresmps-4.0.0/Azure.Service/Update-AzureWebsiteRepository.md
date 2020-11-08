---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015843"
---
# <span data-ttu-id="53fef-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="53fef-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="53fef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53fef-102">SYNOPSIS</span></span>
<span data-ttu-id="53fef-103">Frissíti egy helyi git-tárház távoli tárházait az összes bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="53fef-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="53fef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53fef-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53fef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53fef-105">DESCRIPTION</span></span>
<span data-ttu-id="53fef-106">Az **Update-AzureWebsiteRepository** parancsmag egy helyi git tárház távoli tárházait frissíti a résidők számára.</span><span class="sxs-lookup"><span data-stu-id="53fef-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="53fef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53fef-107">EXAMPLES</span></span>

### <span data-ttu-id="53fef-108">1. példa: reupdate website Remote tárolók</span><span class="sxs-lookup"><span data-stu-id="53fef-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="53fef-109">Frissíti a helyi git-tárház távoli tárházait a webhelyek MyWebsite összes bővítőhelyéhez.</span><span class="sxs-lookup"><span data-stu-id="53fef-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="53fef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53fef-110">PARAMETERS</span></span>

### <span data-ttu-id="53fef-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53fef-111">-Name</span></span>
<span data-ttu-id="53fef-112">A webhely neve.</span><span class="sxs-lookup"><span data-stu-id="53fef-112">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fef-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="53fef-113">-Profile</span></span>
<span data-ttu-id="53fef-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="53fef-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53fef-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="53fef-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53fef-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="53fef-116">-PublishingUsername</span></span>
<span data-ttu-id="53fef-117">A Microsoft Azure Portal for git telepítéséhez megadott Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="53fef-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fef-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53fef-118">-Confirm</span></span>
<span data-ttu-id="53fef-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53fef-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53fef-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53fef-120">-WhatIf</span></span>
<span data-ttu-id="53fef-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53fef-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53fef-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53fef-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53fef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fef-123">CommonParameters</span></span>
<span data-ttu-id="53fef-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53fef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fef-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53fef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fef-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53fef-126">INPUTS</span></span>

## <span data-ttu-id="53fef-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53fef-127">OUTPUTS</span></span>

## <span data-ttu-id="53fef-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53fef-128">NOTES</span></span>

## <span data-ttu-id="53fef-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53fef-129">RELATED LINKS</span></span>

[<span data-ttu-id="53fef-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53fef-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="53fef-131">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53fef-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="53fef-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53fef-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="53fef-133">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53fef-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


