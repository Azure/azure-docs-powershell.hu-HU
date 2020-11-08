---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016067"
---
# <span data-ttu-id="93555-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93555-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="93555-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93555-102">SYNOPSIS</span></span>
<span data-ttu-id="93555-103">Egy Azure virtuális gépen az elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93555-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="93555-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93555-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="93555-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93555-105">DESCRIPTION</span></span>
<span data-ttu-id="93555-106">A **set-AzureAvailabilitySet** parancsmag a központi telepítést követően egy Azure virtuális gépen elérhető elérhetőségi érték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93555-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="93555-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93555-107">EXAMPLES</span></span>

### <span data-ttu-id="93555-108">Példa 1: elérhetőségi készlet nevének módosítása</span><span class="sxs-lookup"><span data-stu-id="93555-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="93555-109">Az első parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="93555-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="93555-110">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="93555-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93555-111">Ez a parancsmag módosítja az adott virtuális gép elérhetőségi készletének a nevét.</span><span class="sxs-lookup"><span data-stu-id="93555-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="93555-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="93555-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="93555-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93555-113">PARAMETERS</span></span>

### <span data-ttu-id="93555-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="93555-114">-AvailabilitySetName</span></span>
<span data-ttu-id="93555-115">Annak az elérhetőségi készletnek a nevét adja meg, amelyhez a virtuális gép tartozik.</span><span class="sxs-lookup"><span data-stu-id="93555-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93555-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="93555-116">-InformationAction</span></span>
<span data-ttu-id="93555-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="93555-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="93555-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="93555-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93555-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="93555-119">Continue</span></span>
- <span data-ttu-id="93555-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="93555-120">Ignore</span></span>
- <span data-ttu-id="93555-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="93555-121">Inquire</span></span>
- <span data-ttu-id="93555-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93555-122">SilentlyContinue</span></span>
- <span data-ttu-id="93555-123">állj</span><span class="sxs-lookup"><span data-stu-id="93555-123">Stop</span></span>
- <span data-ttu-id="93555-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="93555-124">Suspend</span></span>

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

### <span data-ttu-id="93555-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93555-125">-InformationVariable</span></span>
<span data-ttu-id="93555-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="93555-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93555-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="93555-127">-Profile</span></span>
<span data-ttu-id="93555-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="93555-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93555-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="93555-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93555-130">-VM</span><span class="sxs-lookup"><span data-stu-id="93555-130">-VM</span></span>
<span data-ttu-id="93555-131">A virtuális gép azon konfigurációját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="93555-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="93555-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93555-132">CommonParameters</span></span>
<span data-ttu-id="93555-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93555-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93555-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93555-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93555-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93555-135">INPUTS</span></span>

## <span data-ttu-id="93555-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93555-136">OUTPUTS</span></span>

## <span data-ttu-id="93555-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93555-137">NOTES</span></span>

## <span data-ttu-id="93555-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93555-138">RELATED LINKS</span></span>

[<span data-ttu-id="93555-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="93555-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="93555-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93555-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


