---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016130"
---
# <span data-ttu-id="8e2d0-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="8e2d0-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="8e2d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2d0-103">Egy névtér eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-103">Removes a namespace.</span></span>

## <span data-ttu-id="8e2d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e2d0-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2d0-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8e2d0-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8e2d0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8e2d0-108">A **Remove-AzureSBNamespace** parancsmag a Service Bus szolgáltatás névterét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="8e2d0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e2d0-109">EXAMPLES</span></span>

## <span data-ttu-id="8e2d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e2d0-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2d0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8e2d0-111">-Force</span></span>
<span data-ttu-id="8e2d0-112">Ha engedélyezve van, a névtér eltávolítása a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8e2d0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e2d0-113">-Name</span></span>
<span data-ttu-id="8e2d0-114">Az eltávolítandó névtér nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-114">Specifies the name of the namespace to be removed.</span></span>

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

### <span data-ttu-id="8e2d0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e2d0-115">-PassThru</span></span>
<span data-ttu-id="8e2d0-116">A művelet eredménye igaz, ha sikerül.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="8e2d0-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8e2d0-117">-Profile</span></span>
<span data-ttu-id="8e2d0-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e2d0-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e2d0-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e2d0-120">-Confirm</span></span>
<span data-ttu-id="8e2d0-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2d0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2d0-122">-WhatIf</span></span>
<span data-ttu-id="8e2d0-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e2d0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2d0-125">CommonParameters</span></span>
<span data-ttu-id="8e2d0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e2d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2d0-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2d0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2d0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2d0-128">INPUTS</span></span>

## <span data-ttu-id="8e2d0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2d0-129">OUTPUTS</span></span>

## <span data-ttu-id="8e2d0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e2d0-130">NOTES</span></span>

## <span data-ttu-id="8e2d0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e2d0-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e2d0-132">Új – AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="8e2d0-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


