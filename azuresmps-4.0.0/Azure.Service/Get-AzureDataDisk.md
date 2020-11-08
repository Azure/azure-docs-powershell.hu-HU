---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015651"
---
# <span data-ttu-id="19131-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="19131-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="19131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19131-102">SYNOPSIS</span></span>
<span data-ttu-id="19131-103">Azure-adatlemezeket kap.</span><span class="sxs-lookup"><span data-stu-id="19131-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="19131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19131-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19131-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19131-105">DESCRIPTION</span></span>
<span data-ttu-id="19131-106">A **Get-AzureDataDisk** parancsmag olyan objektumot kap, amely az Azure Virtual Machine adatlemezeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="19131-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="19131-107">Ha egy adott adatlemez-objektumot szeretne beszerezni, adja meg a merevlemez logikai egységének számát (LUN).</span><span class="sxs-lookup"><span data-stu-id="19131-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="19131-108">Példák</span><span class="sxs-lookup"><span data-stu-id="19131-108">EXAMPLES</span></span>

### <span data-ttu-id="19131-109">Példa 1: a virtuális gép minden adatlemezének beolvasása</span><span class="sxs-lookup"><span data-stu-id="19131-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="19131-110">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="19131-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="19131-111">A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.</span><span class="sxs-lookup"><span data-stu-id="19131-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19131-112">Az aktuális parancsmag a virtuális gép összes adatlemezét beilleszti.</span><span class="sxs-lookup"><span data-stu-id="19131-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="19131-113">2. példa: adott adatlemez beszerzése egy vituralvirtual-machinevirtual</span><span class="sxs-lookup"><span data-stu-id="19131-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="19131-114">Ez a parancs a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19131-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="19131-115">A parancs átadja a virtuális gépet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="19131-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="19131-116">Az aktuális parancsmag a LUN 2 tároló adatlemezét kapja.</span><span class="sxs-lookup"><span data-stu-id="19131-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="19131-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19131-117">PARAMETERS</span></span>

### <span data-ttu-id="19131-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="19131-118">-InformationAction</span></span>
<span data-ttu-id="19131-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="19131-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19131-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="19131-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19131-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="19131-121">Continue</span></span>
- <span data-ttu-id="19131-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="19131-122">Ignore</span></span>
- <span data-ttu-id="19131-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="19131-123">Inquire</span></span>
- <span data-ttu-id="19131-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19131-124">SilentlyContinue</span></span>
- <span data-ttu-id="19131-125">állj</span><span class="sxs-lookup"><span data-stu-id="19131-125">Stop</span></span>
- <span data-ttu-id="19131-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="19131-126">Suspend</span></span>

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

### <span data-ttu-id="19131-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19131-127">-InformationVariable</span></span>
<span data-ttu-id="19131-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="19131-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19131-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="19131-129">-Lun</span></span>
<span data-ttu-id="19131-130">A virtuális gép adatmeghajtójának logikai egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19131-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="19131-131">Az érvényes értékek a következők: 0 – 15.</span><span class="sxs-lookup"><span data-stu-id="19131-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19131-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="19131-132">-Profile</span></span>
<span data-ttu-id="19131-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="19131-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19131-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="19131-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19131-135">-VM</span><span class="sxs-lookup"><span data-stu-id="19131-135">-VM</span></span>
<span data-ttu-id="19131-136">Annak a virtuális gépnek az objektumát adja meg, amelyhez ez a parancsmag adatlemezeket kap.</span><span class="sxs-lookup"><span data-stu-id="19131-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="19131-137">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="19131-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="19131-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19131-138">CommonParameters</span></span>
<span data-ttu-id="19131-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19131-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19131-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19131-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19131-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19131-141">INPUTS</span></span>

## <span data-ttu-id="19131-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19131-142">OUTPUTS</span></span>

## <span data-ttu-id="19131-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19131-143">NOTES</span></span>

## <span data-ttu-id="19131-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19131-144">RELATED LINKS</span></span>

[<span data-ttu-id="19131-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="19131-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="19131-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="19131-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="19131-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="19131-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="19131-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="19131-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


