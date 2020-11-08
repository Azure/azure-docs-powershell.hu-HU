---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015771"
---
# <span data-ttu-id="e55bf-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-101">Start-AzureVM</span></span>

## <span data-ttu-id="e55bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e55bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e55bf-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="e55bf-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e55bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e55bf-104">SYNTAX</span></span>

### <span data-ttu-id="e55bf-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e55bf-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e55bf-106">Beviteli</span><span class="sxs-lookup"><span data-stu-id="e55bf-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e55bf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e55bf-107">DESCRIPTION</span></span>
<span data-ttu-id="e55bf-108">A **Start-AzureVM** parancsmag az Azure Virtual Machine kezdetét kéri.</span><span class="sxs-lookup"><span data-stu-id="e55bf-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="e55bf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e55bf-109">EXAMPLES</span></span>

### <span data-ttu-id="e55bf-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="e55bf-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="e55bf-111">Ez a parancs elindítja a VirtualMachine04 nevű virtuális gépet, amely a ContosoService03 nevű Azure-szolgáltatásban fut.</span><span class="sxs-lookup"><span data-stu-id="e55bf-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="e55bf-112">2. példa: virtuális gép indítása virtuálisgép-objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="e55bf-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="e55bf-113">Ez a parancs beolvassa a virtuális gép objektumát annak a virtuális gépnek, amelynek a neve adatbázis kiszolgálója, majd indítsa el a kérést.</span><span class="sxs-lookup"><span data-stu-id="e55bf-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="e55bf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e55bf-114">PARAMETERS</span></span>

### <span data-ttu-id="e55bf-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e55bf-115">-InformationAction</span></span>
<span data-ttu-id="e55bf-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e55bf-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e55bf-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e55bf-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e55bf-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e55bf-118">Continue</span></span>
- <span data-ttu-id="e55bf-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e55bf-119">Ignore</span></span>
- <span data-ttu-id="e55bf-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e55bf-120">Inquire</span></span>
- <span data-ttu-id="e55bf-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e55bf-121">SilentlyContinue</span></span>
- <span data-ttu-id="e55bf-122">állj</span><span class="sxs-lookup"><span data-stu-id="e55bf-122">Stop</span></span>
- <span data-ttu-id="e55bf-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e55bf-123">Suspend</span></span>

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

### <span data-ttu-id="e55bf-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e55bf-124">-InformationVariable</span></span>
<span data-ttu-id="e55bf-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e55bf-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e55bf-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e55bf-126">-Name</span></span>
<span data-ttu-id="e55bf-127">A elindítani kívánt virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e55bf-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e55bf-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="e55bf-128">-Profile</span></span>
<span data-ttu-id="e55bf-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e55bf-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e55bf-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e55bf-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e55bf-131">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e55bf-131">-ServiceName</span></span>
<span data-ttu-id="e55bf-132">Annak az Azure-szolgáltatásnak a nevét adja meg, amely az elindítani kívánt virtuális gépet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e55bf-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="e55bf-133">-VM</span><span class="sxs-lookup"><span data-stu-id="e55bf-133">-VM</span></span>
<span data-ttu-id="e55bf-134">Olyan virtuálisgép-objektumot ad meg, amely azonosítja a virtuális gépet a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="e55bf-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e55bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55bf-135">CommonParameters</span></span>
<span data-ttu-id="e55bf-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e55bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55bf-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e55bf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55bf-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e55bf-138">INPUTS</span></span>

## <span data-ttu-id="e55bf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e55bf-139">OUTPUTS</span></span>

## <span data-ttu-id="e55bf-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e55bf-140">NOTES</span></span>

## <span data-ttu-id="e55bf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e55bf-141">RELATED LINKS</span></span>

[<span data-ttu-id="e55bf-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e55bf-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="e55bf-144">Újraindítás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="e55bf-145">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="e55bf-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e55bf-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


