---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017398"
---
# <span data-ttu-id="10977-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-101">New-WAPackVM</span></span>

## <span data-ttu-id="10977-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10977-102">SYNOPSIS</span></span>
<span data-ttu-id="10977-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="10977-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="10977-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10977-104">SYNTAX</span></span>

### <span data-ttu-id="10977-105">CreateVMFromTemplate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10977-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10977-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="10977-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10977-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="10977-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10977-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="10977-108">DESCRIPTION</span></span>
<span data-ttu-id="10977-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="10977-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="10977-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="10977-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10977-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10977-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10977-112">A **New-WAPackVM** parancsmag virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="10977-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="10977-113">Példák</span><span class="sxs-lookup"><span data-stu-id="10977-113">EXAMPLES</span></span>

### <span data-ttu-id="10977-114">Példa 1: virtuális gép létrehozása Windows operációs rendszerhez sablon használatával</span><span class="sxs-lookup"><span data-stu-id="10977-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="10977-115">Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="10977-116">A parancsmag a fiók és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="10977-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="10977-117">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="10977-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="10977-118">A második parancs a **Get-WAPackVMTemplate** parancsmag használatával kapja meg a ContosoTemplate04 nevű virtuálisgép-sablont, majd a $Template változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="10977-119">A végleges parancs létrehoz egy ContosoV023 nevű virtuális gépet a $Template változóban tárolt sablon alapján.</span><span class="sxs-lookup"><span data-stu-id="10977-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="10977-120">A parancs a *Windows* paramétert adja meg, ezért a virtuális gépnek futnia kell a Windows operációs rendszer verziójától.</span><span class="sxs-lookup"><span data-stu-id="10977-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="10977-121">2. példa: virtuális gép létrehozása Linux operációs rendszerhez sablon használatával</span><span class="sxs-lookup"><span data-stu-id="10977-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="10977-122">Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="10977-123">A második parancs a **Get-WAPackVMTemplate** parancsmag használatával kapja meg a ContosoTemplate19 nevű virtuálisgép-sablont, majd a $Template változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="10977-124">A végleges parancs létrehoz egy ContosoV028 nevű virtuális gépet a $Template változóban tárolt sablon alapján.</span><span class="sxs-lookup"><span data-stu-id="10977-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="10977-125">A parancs a *Linux* paramétert adja meg, ezért a virtuális gépnek a Linux operációs rendszer verzióját kell futtatnia.</span><span class="sxs-lookup"><span data-stu-id="10977-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="10977-126">3. példa: virtuális gép létrehozása operációs rendszerbeli lemezről és méretről</span><span class="sxs-lookup"><span data-stu-id="10977-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="10977-127">Az első parancs a **Get-WAPackVMOSDisk** parancsmaggal a ContosoDiskOS nevű operációs rendszer lemezét kapja, majd a $OSDisk változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="10977-128">A második parancs a **Get-WAPackVMSizeProfile** parancsmaggal kapja meg a MediumSizeVM nevű méret profilt, majd a $SizeProfile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10977-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="10977-129">A végleges parancs létrehoz egy ContosoV073 nevű virtuális gépet az $OSDisk tárolt operációs rendszerről és a $SizeProfile tárolt méret profilról.</span><span class="sxs-lookup"><span data-stu-id="10977-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="10977-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10977-130">PARAMETERS</span></span>

### <span data-ttu-id="10977-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="10977-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="10977-132">A rendszergazdai fiók Secure Shell (SSH) kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10977-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="10977-133">-Linux</span></span>
<span data-ttu-id="10977-134">Azt jelzi, hogy a parancsmag virtuális gépet hoz létre a Linux operációs rendszer futtatásához.</span><span class="sxs-lookup"><span data-stu-id="10977-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10977-135">-Name</span></span>
<span data-ttu-id="10977-136">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10977-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="10977-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="10977-137">-OSDisk</span></span>
<span data-ttu-id="10977-138">Az operációs rendszer merevlemezét adja meg **VirtualHardDisk** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="10977-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="10977-139">Operációs rendszer lemezének beszerzéséhez használja a **Get-WAPackVMOSDisk** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10977-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-140">-Termék</span><span class="sxs-lookup"><span data-stu-id="10977-140">-ProductKey</span></span>
<span data-ttu-id="10977-141">A termékkulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="10977-141">Specifies a product key.</span></span>
<span data-ttu-id="10977-142">A termékkulcs egy 25 jegyből álló szám, amely azonosítja a termék licencét.</span><span class="sxs-lookup"><span data-stu-id="10977-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="10977-143">Termékkulcs használata egy olyan operációs rendszerhez, amelyet virtuális gépre vagy állomásra tervez telepíteni.</span><span class="sxs-lookup"><span data-stu-id="10977-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="10977-144">-Profile</span></span>
<span data-ttu-id="10977-145">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="10977-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10977-146">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="10977-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10977-147">-Sablon</span><span class="sxs-lookup"><span data-stu-id="10977-147">-Template</span></span>
<span data-ttu-id="10977-148">Egy sablont ad meg.</span><span class="sxs-lookup"><span data-stu-id="10977-148">Specifies a template.</span></span>
<span data-ttu-id="10977-149">A parancsmag a megadott sablonon alapuló virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="10977-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="10977-150">A Template-objektum beolvasásához használja az Get-WAPackVMTemplate parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10977-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="10977-151">-VMCredential</span></span>
<span data-ttu-id="10977-152">A helyi rendszergazdai fiók hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="10977-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="10977-153">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10977-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="10977-154">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="10977-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="10977-155">-VMSizeProfile</span></span>
<span data-ttu-id="10977-156">A virtuális gép **HardwareProfile** -objektumként használt méret profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="10977-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="10977-157">Ha szeretné beolvasni a méretet, használja a **Get-WAPackVMSizeProfile** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10977-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="10977-158">-VNet</span></span>
<span data-ttu-id="10977-159">Virtuális hálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="10977-159">Specifies a virtual network.</span></span>
<span data-ttu-id="10977-160">A parancsmag a virtuális gépet a megadott virtuális hálózathoz köti.</span><span class="sxs-lookup"><span data-stu-id="10977-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="10977-161">Virtuális hálózat beszerzéséhez használja a **Get-WAPackVNet** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10977-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="10977-162">-Windows</span></span>
<span data-ttu-id="10977-163">Azt jelzi, hogy a parancsmag virtuális gépet hoz létre a Windows operációs rendszer futtatásához.</span><span class="sxs-lookup"><span data-stu-id="10977-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10977-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10977-164">CommonParameters</span></span>
<span data-ttu-id="10977-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10977-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10977-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10977-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10977-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10977-167">INPUTS</span></span>

## <span data-ttu-id="10977-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10977-168">OUTPUTS</span></span>

## <span data-ttu-id="10977-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10977-169">NOTES</span></span>

## <span data-ttu-id="10977-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10977-170">RELATED LINKS</span></span>

[<span data-ttu-id="10977-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="10977-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="10977-173">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="10977-174">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="10977-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="10977-176">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="10977-177">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="10977-178">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10977-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="10977-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="10977-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="10977-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="10977-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="10977-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="10977-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


