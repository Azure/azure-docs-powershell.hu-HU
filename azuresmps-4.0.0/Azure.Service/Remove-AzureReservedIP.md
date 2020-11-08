---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016145"
---
# <span data-ttu-id="fface-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fface-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="fface-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fface-102">SYNOPSIS</span></span>
<span data-ttu-id="fface-103">Eltávolítja a lefoglalt IP-címet a neve alapján.</span><span class="sxs-lookup"><span data-stu-id="fface-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="fface-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fface-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fface-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fface-105">DESCRIPTION</span></span>
<span data-ttu-id="fface-106">A **Remove-AzureReservedIP** parancsmag a lefoglalt IP-címet a neve alapján távolítja el.</span><span class="sxs-lookup"><span data-stu-id="fface-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="fface-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fface-107">EXAMPLES</span></span>

### <span data-ttu-id="fface-108">1. példa: fenntartott IP-cím eltávolítása a nevével</span><span class="sxs-lookup"><span data-stu-id="fface-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="fface-109">Ez a parancs eltávolítja a lefoglalt IP-címet a neve alapján.</span><span class="sxs-lookup"><span data-stu-id="fface-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="fface-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fface-110">PARAMETERS</span></span>

### <span data-ttu-id="fface-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fface-111">-Force</span></span>
<span data-ttu-id="fface-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fface-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fface-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fface-113">-InformationAction</span></span>
<span data-ttu-id="fface-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="fface-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fface-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fface-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fface-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="fface-116">Continue</span></span>
- <span data-ttu-id="fface-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="fface-117">Ignore</span></span>
- <span data-ttu-id="fface-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="fface-118">Inquire</span></span>
- <span data-ttu-id="fface-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fface-119">SilentlyContinue</span></span>
- <span data-ttu-id="fface-120">állj</span><span class="sxs-lookup"><span data-stu-id="fface-120">Stop</span></span>
- <span data-ttu-id="fface-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="fface-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fface-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fface-122">-InformationVariable</span></span>
<span data-ttu-id="fface-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="fface-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fface-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="fface-124">-Profile</span></span>
<span data-ttu-id="fface-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fface-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fface-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fface-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fface-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="fface-127">-ReservedIPName</span></span>
<span data-ttu-id="fface-128">A foglalt IP-cím nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fface-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fface-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fface-129">CommonParameters</span></span>
<span data-ttu-id="fface-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fface-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fface-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fface-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fface-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fface-132">INPUTS</span></span>

## <span data-ttu-id="fface-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fface-133">OUTPUTS</span></span>

## <span data-ttu-id="fface-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fface-134">NOTES</span></span>

## <span data-ttu-id="fface-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fface-135">RELATED LINKS</span></span>

[<span data-ttu-id="fface-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fface-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="fface-137">Új – AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fface-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="fface-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="fface-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


