---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015483"
---
# <span data-ttu-id="2027e-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2027e-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="2027e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2027e-102">SYNOPSIS</span></span>
<span data-ttu-id="2027e-103">Eltávolítja a megadott webhelyet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="2027e-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="2027e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2027e-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2027e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2027e-105">DESCRIPTION</span></span>
<span data-ttu-id="2027e-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="2027e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2027e-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2027e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2027e-108">A **Remove-AzureWebsite** parancsmag eltávolítja a megadott webhelyet az Azure-ról a megerősítési kéréssel vagy anélkül.</span><span class="sxs-lookup"><span data-stu-id="2027e-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="2027e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2027e-109">EXAMPLES</span></span>

### <span data-ttu-id="2027e-110">1. példa: az aktuális webhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2027e-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="2027e-111">Ez a példa eltávolítja az Azure webhelyét az aktuális címtárral társítva.</span><span class="sxs-lookup"><span data-stu-id="2027e-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="2027e-112">2. példa: webhely eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="2027e-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="2027e-113">Ez a példa törli a mySite nevű webhelyet a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2027e-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="2027e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2027e-114">PARAMETERS</span></span>

### <span data-ttu-id="2027e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2027e-115">-Force</span></span>
<span data-ttu-id="2027e-116">Ha meg van adva, a megadott webhely törlése megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2027e-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2027e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2027e-117">-Name</span></span>
<span data-ttu-id="2027e-118">Annak a webhelynek a neve, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="2027e-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="2027e-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="2027e-119">-Profile</span></span>
<span data-ttu-id="2027e-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2027e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2027e-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2027e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2027e-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="2027e-122">-Slot</span></span>
<span data-ttu-id="2027e-123">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2027e-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="2027e-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2027e-124">-Confirm</span></span>
<span data-ttu-id="2027e-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2027e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2027e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2027e-126">-WhatIf</span></span>
<span data-ttu-id="2027e-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2027e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2027e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2027e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2027e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2027e-129">CommonParameters</span></span>
<span data-ttu-id="2027e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2027e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2027e-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2027e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2027e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2027e-132">INPUTS</span></span>

## <span data-ttu-id="2027e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2027e-133">OUTPUTS</span></span>

## <span data-ttu-id="2027e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2027e-134">NOTES</span></span>

## <span data-ttu-id="2027e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2027e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2027e-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2027e-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


