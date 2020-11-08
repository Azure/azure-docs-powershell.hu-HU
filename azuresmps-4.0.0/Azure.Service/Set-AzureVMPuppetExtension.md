---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015849"
---
# <span data-ttu-id="71122-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="71122-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="71122-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71122-102">SYNOPSIS</span></span>
<span data-ttu-id="71122-103">Egy virtuális gép báb-kiterjesztését állítja be.</span><span class="sxs-lookup"><span data-stu-id="71122-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="71122-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71122-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="71122-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71122-105">DESCRIPTION</span></span>
<span data-ttu-id="71122-106">A **set-AzureVMPuppetExtension** parancsmag a virtuális gép báb-kiterjesztését állítja be.</span><span class="sxs-lookup"><span data-stu-id="71122-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="71122-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71122-107">EXAMPLES</span></span>

### <span data-ttu-id="71122-108">Példa 1: a báb-kiterjesztés beállítása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="71122-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="71122-109">Ebben a példában a megadott virtuális gép báb-kiterjesztését állítja be a $VM változóban tárolt módon.</span><span class="sxs-lookup"><span data-stu-id="71122-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="71122-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71122-110">PARAMETERS</span></span>

### <span data-ttu-id="71122-111">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="71122-111">-Disable</span></span>
<span data-ttu-id="71122-112">Jelzi, hogy ez a parancsmag letiltja a bővítmény állapotát.</span><span class="sxs-lookup"><span data-stu-id="71122-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71122-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71122-113">-InformationAction</span></span>
<span data-ttu-id="71122-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="71122-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71122-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="71122-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71122-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="71122-116">Continue</span></span>
- <span data-ttu-id="71122-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="71122-117">Ignore</span></span>
- <span data-ttu-id="71122-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="71122-118">Inquire</span></span>
- <span data-ttu-id="71122-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71122-119">SilentlyContinue</span></span>
- <span data-ttu-id="71122-120">állj</span><span class="sxs-lookup"><span data-stu-id="71122-120">Stop</span></span>
- <span data-ttu-id="71122-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="71122-121">Suspend</span></span>

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

### <span data-ttu-id="71122-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71122-122">-InformationVariable</span></span>
<span data-ttu-id="71122-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="71122-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71122-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="71122-124">-Profile</span></span>
<span data-ttu-id="71122-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="71122-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71122-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="71122-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71122-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="71122-127">-PuppetMasterServer</span></span>
<span data-ttu-id="71122-128">A báb-főkiszolgáló teljes tartománynevét adja meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="71122-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="71122-129">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="71122-129">-ReferenceName</span></span>
<span data-ttu-id="71122-130">A kiterjesztés hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71122-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="71122-131">Ez egy felhasználó által definiált karakterlánc, amely a kiterjesztésre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="71122-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="71122-132">A program akkor adja meg, ha a bővítményt első alkalommal felveszi a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="71122-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="71122-133">A későbbi frissítésekhez a bővítmény frissítésekor meg kell adnia a korábban használt hivatkozási nevet.</span><span class="sxs-lookup"><span data-stu-id="71122-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="71122-134">A bővítményhez rendelt hivatkozásnév a **Get-AzureVM** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="71122-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71122-135">-Verzió</span><span class="sxs-lookup"><span data-stu-id="71122-135">-Version</span></span>
<span data-ttu-id="71122-136">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71122-136">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71122-137">-VM</span><span class="sxs-lookup"><span data-stu-id="71122-137">-VM</span></span>
<span data-ttu-id="71122-138">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="71122-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="71122-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71122-139">CommonParameters</span></span>
<span data-ttu-id="71122-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71122-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71122-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71122-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71122-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71122-142">INPUTS</span></span>

## <span data-ttu-id="71122-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71122-143">OUTPUTS</span></span>

## <span data-ttu-id="71122-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71122-144">NOTES</span></span>

## <span data-ttu-id="71122-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71122-145">RELATED LINKS</span></span>

[<span data-ttu-id="71122-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="71122-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


