---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016172"
---
# <span data-ttu-id="e6227-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e6227-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="e6227-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6227-102">SYNOPSIS</span></span>
<span data-ttu-id="e6227-103">Az előfizetésben szereplő affinitási csoport törlése</span><span class="sxs-lookup"><span data-stu-id="e6227-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="e6227-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6227-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6227-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6227-105">DESCRIPTION</span></span>
<span data-ttu-id="e6227-106">A **Remove-AzureAffinityGroup** parancsmag az Azure affinitási csoportot törli az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e6227-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="e6227-107">A tagokat tartalmazó affinitási csoportok nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="e6227-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="e6227-108">Először törölnie kell az affinitás csoport tagjait.</span><span class="sxs-lookup"><span data-stu-id="e6227-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="e6227-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e6227-109">EXAMPLES</span></span>

### <span data-ttu-id="e6227-110">1. példa: affinitási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6227-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="e6227-111">Ez a parancs törli a South01-affinitás csoportot az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e6227-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="e6227-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6227-112">PARAMETERS</span></span>

### <span data-ttu-id="e6227-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e6227-113">-InformationAction</span></span>
<span data-ttu-id="e6227-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e6227-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6227-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e6227-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6227-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e6227-116">Continue</span></span>
- <span data-ttu-id="e6227-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e6227-117">Ignore</span></span>
- <span data-ttu-id="e6227-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e6227-118">Inquire</span></span>
- <span data-ttu-id="e6227-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6227-119">SilentlyContinue</span></span>
- <span data-ttu-id="e6227-120">állj</span><span class="sxs-lookup"><span data-stu-id="e6227-120">Stop</span></span>
- <span data-ttu-id="e6227-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e6227-121">Suspend</span></span>

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

### <span data-ttu-id="e6227-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6227-122">-InformationVariable</span></span>
<span data-ttu-id="e6227-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e6227-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e6227-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6227-124">-Name</span></span>
<span data-ttu-id="e6227-125">A parancsmag által törölt affinitási csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6227-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e6227-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6227-126">-Profile</span></span>
<span data-ttu-id="e6227-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e6227-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6227-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e6227-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6227-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6227-129">CommonParameters</span></span>
<span data-ttu-id="e6227-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6227-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6227-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6227-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6227-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6227-132">INPUTS</span></span>

## <span data-ttu-id="e6227-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6227-133">OUTPUTS</span></span>

## <span data-ttu-id="e6227-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6227-134">NOTES</span></span>

## <span data-ttu-id="e6227-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6227-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6227-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e6227-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="e6227-137">Új – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e6227-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="e6227-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e6227-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


