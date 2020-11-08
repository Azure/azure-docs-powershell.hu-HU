---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015791"
---
# <span data-ttu-id="43fa6-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="43fa6-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="43fa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="43fa6-103">Egy Azure virtuális gép méretének beállítását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="43fa6-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="43fa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43fa6-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43fa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="43fa6-106">A **set-AzureVMSize** parancsmag frissíti a virtuális gép méretét.</span><span class="sxs-lookup"><span data-stu-id="43fa6-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="43fa6-107">Két paramétere van: *InstanceSize* , amely a virtuális gép új mérete, és a *VM* , amely a Virtual Machine objektum a **Get-AzureVM** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="43fa6-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="43fa6-108">A **set-AzureVMSize** eredménye a **Update-AzureVM** parancsmagra, illetve egy változóban későbbi használat céljából tárolható.</span><span class="sxs-lookup"><span data-stu-id="43fa6-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="43fa6-109">A **frissítési AzureVM** végrehajtása csak akkor történik meg, ha nincs tényleges módosítás.</span><span class="sxs-lookup"><span data-stu-id="43fa6-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="43fa6-110">Megjegyzés: Ez a parancsmag megköveteli a virtuális gép újralétesítését és új IP-cím megadását is.</span><span class="sxs-lookup"><span data-stu-id="43fa6-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="43fa6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="43fa6-111">EXAMPLES</span></span>

### <span data-ttu-id="43fa6-112">Példa 1: virtuális gép méretének beállítása</span><span class="sxs-lookup"><span data-stu-id="43fa6-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="43fa6-113">A parancs frissíti a virtuális gépet a "kicsi" méretre.</span><span class="sxs-lookup"><span data-stu-id="43fa6-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="43fa6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43fa6-114">PARAMETERS</span></span>

### <span data-ttu-id="43fa6-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43fa6-115">-InformationAction</span></span>
<span data-ttu-id="43fa6-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="43fa6-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43fa6-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="43fa6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43fa6-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="43fa6-118">Continue</span></span>
- <span data-ttu-id="43fa6-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="43fa6-119">Ignore</span></span>
- <span data-ttu-id="43fa6-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="43fa6-120">Inquire</span></span>
- <span data-ttu-id="43fa6-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43fa6-121">SilentlyContinue</span></span>
- <span data-ttu-id="43fa6-122">állj</span><span class="sxs-lookup"><span data-stu-id="43fa6-122">Stop</span></span>
- <span data-ttu-id="43fa6-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="43fa6-123">Suspend</span></span>

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

### <span data-ttu-id="43fa6-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43fa6-124">-InformationVariable</span></span>
<span data-ttu-id="43fa6-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="43fa6-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43fa6-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="43fa6-126">-InstanceSize</span></span>
<span data-ttu-id="43fa6-127">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43fa6-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="43fa6-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="43fa6-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="43fa6-129">---ExtraSmall-------------------------------ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="43fa6-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="43fa6-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="43fa6-130">-Profile</span></span>
<span data-ttu-id="43fa6-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="43fa6-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43fa6-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="43fa6-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43fa6-133">-VM</span><span class="sxs-lookup"><span data-stu-id="43fa6-133">-VM</span></span>
<span data-ttu-id="43fa6-134">Annak a virtuális számítógép-objektumnak a meghatározása, amelyre a parancsmag beállítja a méretet.</span><span class="sxs-lookup"><span data-stu-id="43fa6-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43fa6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fa6-135">CommonParameters</span></span>
<span data-ttu-id="43fa6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43fa6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fa6-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fa6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fa6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43fa6-138">INPUTS</span></span>

## <span data-ttu-id="43fa6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43fa6-139">OUTPUTS</span></span>

## <span data-ttu-id="43fa6-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43fa6-140">NOTES</span></span>

## <span data-ttu-id="43fa6-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43fa6-141">RELATED LINKS</span></span>

[<span data-ttu-id="43fa6-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="43fa6-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="43fa6-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="43fa6-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


