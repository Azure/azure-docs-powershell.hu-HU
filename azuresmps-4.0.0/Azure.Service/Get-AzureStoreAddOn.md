---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015547"
---
# <span data-ttu-id="b7fb8-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="b7fb8-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="b7fb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fb8-103">Az elérhető Azure Store bővítmények beolvasása</span><span class="sxs-lookup"><span data-stu-id="b7fb8-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="b7fb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7fb8-104">SYNTAX</span></span>

### <span data-ttu-id="b7fb8-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b7fb8-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b7fb8-106">GetAddOn</span><span class="sxs-lookup"><span data-stu-id="b7fb8-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7fb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="b7fb8-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b7fb8-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b7fb8-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b7fb8-110">A rendelkezésre álló bővítmények beszerzése az Azure Store áruházból, vagy az aktuális előfizetéshez tartozó meglévő bővítmény-példányok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="b7fb8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b7fb8-111">EXAMPLES</span></span>

### <span data-ttu-id="b7fb8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7fb8-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="b7fb8-113">Ez a példa beolvassa a jelenlegi előfizetés összes megvásárolt bővítmény-példányát.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="b7fb8-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b7fb8-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="b7fb8-115">Ez a példa az Amerikai Egyesült Államokban az Azure Store áruházból beszerezhető összes bővítményt megkapja.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="b7fb8-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="b7fb8-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="b7fb8-117">Ez a példa egy MyAddOn nevű bővítményt kap a jelenlegi előfizetéshez tartozó megvásárolt bővítményről.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="b7fb8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7fb8-118">PARAMETERS</span></span>

### <span data-ttu-id="b7fb8-119">-Ország</span><span class="sxs-lookup"><span data-stu-id="b7fb8-119">-Country</span></span>
<span data-ttu-id="b7fb8-120">Ha meg van adva, akkor csak a megadott országban elérhető Azure Store bővítmény-példányokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="b7fb8-121">Az alapértelmezett érték az "amerikai".</span><span class="sxs-lookup"><span data-stu-id="b7fb8-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fb8-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b7fb8-122">-ListAvailable</span></span>
<span data-ttu-id="b7fb8-123">Ha meg van adva, elérhetővé válik az Azure áruházból beszerezhető bővítmények.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fb8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7fb8-124">-Name</span></span>
<span data-ttu-id="b7fb8-125">A megadott nevű bővítményt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fb8-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="b7fb8-126">-Profile</span></span>
<span data-ttu-id="b7fb8-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7fb8-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b7fb8-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7fb8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fb8-129">CommonParameters</span></span>
<span data-ttu-id="b7fb8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7fb8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fb8-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7fb8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fb8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fb8-132">INPUTS</span></span>

## <span data-ttu-id="b7fb8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fb8-133">OUTPUTS</span></span>

## <span data-ttu-id="b7fb8-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7fb8-134">NOTES</span></span>

## <span data-ttu-id="b7fb8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7fb8-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7fb8-136">Új – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="b7fb8-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="b7fb8-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="b7fb8-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="b7fb8-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="b7fb8-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


