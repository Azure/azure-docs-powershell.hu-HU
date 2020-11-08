---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015939"
---
# <span data-ttu-id="3cc4e-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="3cc4e-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="3cc4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc4e-103">Felcseréli egy másik bővítőhelyet tartalmazó webhelyhez tartozó termelési résidőt.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="3cc4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cc4e-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc4e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cc4e-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc4e-106">A **switch-AzureWebsiteSlot** parancsmag egy másik bővítőhelyet tartalmazó webhely gyártási bővítőhelyét cseréli le.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="3cc4e-107">Ez a funkció csak a két bővítőhelyet használó webhelyeken működik.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="3cc4e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3cc4e-108">EXAMPLES</span></span>

### <span data-ttu-id="3cc4e-109">1. példa: a webhely-tárolóhely váltása</span><span class="sxs-lookup"><span data-stu-id="3cc4e-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="3cc4e-110">Váltson az Azure webhely MyWebsite biztonsági másolati nyílásába a termelési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="3cc4e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cc4e-111">PARAMETERS</span></span>

### <span data-ttu-id="3cc4e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3cc4e-112">-Force</span></span>
<span data-ttu-id="3cc4e-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3cc4e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cc4e-114">-Name</span></span>
<span data-ttu-id="3cc4e-115">A webhely neve.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-115">The name of the website.</span></span>

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

### <span data-ttu-id="3cc4e-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="3cc4e-116">-Profile</span></span>
<span data-ttu-id="3cc4e-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3cc4e-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3cc4e-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="3cc4e-119">-Slot1</span></span>
<span data-ttu-id="3cc4e-120">Az első bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-120">Specifies the first slot.</span></span>

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

### <span data-ttu-id="3cc4e-121">-SLOT2</span><span class="sxs-lookup"><span data-stu-id="3cc4e-121">-Slot2</span></span>
<span data-ttu-id="3cc4e-122">A második bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-122">Specifies the second slot.</span></span>

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

### <span data-ttu-id="3cc4e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3cc4e-123">-Confirm</span></span>
<span data-ttu-id="3cc4e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc4e-125">-WhatIf</span></span>
<span data-ttu-id="3cc4e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc4e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cc4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc4e-128">CommonParameters</span></span>
<span data-ttu-id="3cc4e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cc4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc4e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc4e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc4e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cc4e-131">INPUTS</span></span>

## <span data-ttu-id="3cc4e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cc4e-132">OUTPUTS</span></span>

## <span data-ttu-id="3cc4e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cc4e-133">NOTES</span></span>

## <span data-ttu-id="3cc4e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cc4e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3cc4e-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3cc4e-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="3cc4e-136">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3cc4e-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="3cc4e-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3cc4e-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="3cc4e-138">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3cc4e-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


