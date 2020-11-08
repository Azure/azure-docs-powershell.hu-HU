---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015811"
---
# <span data-ttu-id="b259e-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b259e-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="b259e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b259e-102">SYNOPSIS</span></span>
<span data-ttu-id="b259e-103">Egy virtuális gép VMAccess-bővítményének beállítása.</span><span class="sxs-lookup"><span data-stu-id="b259e-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="b259e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b259e-104">SYNTAX</span></span>

### <span data-ttu-id="b259e-105">EnableAccessExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b259e-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b259e-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b259e-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b259e-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b259e-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b259e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b259e-108">DESCRIPTION</span></span>
<span data-ttu-id="b259e-109">A **set-AzureVMAccessExtension** parancsmag a Virtual Machine VMAccess bővítményt hozzáadja egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b259e-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="b259e-110">Az VMAccess-kiterjesztéssel ideiglenes jelszót állíthat be, ezért ezt azonnal módosítania kell a gépbe való bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="b259e-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="b259e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b259e-111">EXAMPLES</span></span>

### <span data-ttu-id="b259e-112">1. példa: a VMAccess bővítmény beállítása adott virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="b259e-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="b259e-113">Ez a parancs a megadott virtuális gépre alkalmazott VMAccess-bővítményt állítja be a változó $VMben tárolt módon.</span><span class="sxs-lookup"><span data-stu-id="b259e-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="b259e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b259e-114">PARAMETERS</span></span>

### <span data-ttu-id="b259e-115">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="b259e-115">-Disable</span></span>
<span data-ttu-id="b259e-116">Azt jelzi, hogy ez a parancsmag a letiltani kívánt kiterjesztési állapotot állítja be.</span><span class="sxs-lookup"><span data-stu-id="b259e-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="b259e-117">-ForceUpdate</span></span>
<span data-ttu-id="b259e-118">Azt jelzi, hogy ez a parancsmag újra alkalmazza a konfigurációt egy bővítményre, amikor a konfiguráció nem frissült.</span><span class="sxs-lookup"><span data-stu-id="b259e-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b259e-119">-InformationAction</span></span>
<span data-ttu-id="b259e-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b259e-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b259e-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b259e-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b259e-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b259e-122">Continue</span></span>
- <span data-ttu-id="b259e-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b259e-123">Ignore</span></span>
- <span data-ttu-id="b259e-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b259e-124">Inquire</span></span>
- <span data-ttu-id="b259e-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b259e-125">SilentlyContinue</span></span>
- <span data-ttu-id="b259e-126">állj</span><span class="sxs-lookup"><span data-stu-id="b259e-126">Stop</span></span>
- <span data-ttu-id="b259e-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b259e-127">Suspend</span></span>

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

### <span data-ttu-id="b259e-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b259e-128">-InformationVariable</span></span>
<span data-ttu-id="b259e-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b259e-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b259e-130">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b259e-130">-Password</span></span>
<span data-ttu-id="b259e-131">A virtuális gép hitelesítő adatainak alaphelyzetbe állításához szükséges jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b259e-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="b259e-132">-Profile</span></span>
<span data-ttu-id="b259e-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b259e-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b259e-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b259e-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b259e-135">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="b259e-135">-ReferenceName</span></span>
<span data-ttu-id="b259e-136">Az Access-bővítmény hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b259e-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="b259e-137">Ez egy felhasználó által definiált karakterlánc, amely a kiterjesztésre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b259e-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="b259e-138">A program akkor adja meg, ha a bővítményt első alkalommal felveszi a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="b259e-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="b259e-139">A későbbi frissítésekhez a kiterjesztés frissítésekor meg kell adnia a korábban használt hivatkozási nevet.</span><span class="sxs-lookup"><span data-stu-id="b259e-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="b259e-140">A bővítményhez rendelt *hivatkozásnév* a **Get-AzureVM** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="b259e-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-141">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="b259e-141">-Uninstall</span></span>
<span data-ttu-id="b259e-142">Azt jelzi, hogy a parancsmag eltávolítja-e az Access-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="b259e-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-143">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="b259e-143">-UserName</span></span>
<span data-ttu-id="b259e-144">Annak a felhasználónak a nevét adja meg, amely a parancsmag által a virtuális gép hitelesítő adatainak visszaállításához használható.</span><span class="sxs-lookup"><span data-stu-id="b259e-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-145">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b259e-145">-Version</span></span>
<span data-ttu-id="b259e-146">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b259e-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b259e-147">-VM</span><span class="sxs-lookup"><span data-stu-id="b259e-147">-VM</span></span>
<span data-ttu-id="b259e-148">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b259e-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b259e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b259e-149">CommonParameters</span></span>
<span data-ttu-id="b259e-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b259e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b259e-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b259e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b259e-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b259e-152">INPUTS</span></span>

## <span data-ttu-id="b259e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b259e-153">OUTPUTS</span></span>

## <span data-ttu-id="b259e-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b259e-154">NOTES</span></span>

## <span data-ttu-id="b259e-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b259e-155">RELATED LINKS</span></span>

[<span data-ttu-id="b259e-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b259e-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="b259e-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b259e-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


