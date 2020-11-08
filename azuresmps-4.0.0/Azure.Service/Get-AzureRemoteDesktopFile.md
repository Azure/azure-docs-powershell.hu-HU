---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015620"
---
# <span data-ttu-id="aec3e-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="aec3e-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="aec3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aec3e-102">SYNOPSIS</span></span>
<span data-ttu-id="aec3e-103">Az Azure virtuális gép RDP-fájlját kapja.</span><span class="sxs-lookup"><span data-stu-id="aec3e-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="aec3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aec3e-104">SYNTAX</span></span>

### <span data-ttu-id="aec3e-105">Letöltés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aec3e-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="aec3e-106">Rovatok sávon</span><span class="sxs-lookup"><span data-stu-id="aec3e-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="aec3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aec3e-107">DESCRIPTION</span></span>
<span data-ttu-id="aec3e-108">A **Get-AzureRemoteDesktopFile** parancsmag letölti és menti az Azure Virtual Machine Remote Desktop Connection (RDP) fájlt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="aec3e-109">A parancsmag egy távoli asztali kapcsolatot tud indítani a megadott virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="aec3e-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="aec3e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aec3e-110">EXAMPLES</span></span>

### <span data-ttu-id="aec3e-111">Példa 1: RDP-fájl kérése</span><span class="sxs-lookup"><span data-stu-id="aec3e-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="aec3e-112">Ez a parancs egy RDP-fájlt kap a VirtualMachine07 nevű virtuális VirtualMachine07 nevű virtuális gépnek, amely a ContosoService nevű szolgáltatáson fut.</span><span class="sxs-lookup"><span data-stu-id="aec3e-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="aec3e-113">A parancs a fájlt C:\temp\VirtualMachine07.rdp.-ként tárolja</span><span class="sxs-lookup"><span data-stu-id="aec3e-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="aec3e-114">2. példa: távoli munkamenet indítása</span><span class="sxs-lookup"><span data-stu-id="aec3e-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="aec3e-115">Ez a parancs egy RDP-fájlt kap a VirtualMachine07 nevű virtuális VirtualMachine07 nevű virtuális gépnek, amely a ContosoService nevű szolgáltatáson fut.</span><span class="sxs-lookup"><span data-stu-id="aec3e-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="aec3e-116">A parancs elindítja a távoli asztali munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="aec3e-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="aec3e-117">A parancs törli az RDP-fájlt a kapcsolat bezárásakor.</span><span class="sxs-lookup"><span data-stu-id="aec3e-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="aec3e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aec3e-118">PARAMETERS</span></span>

### <span data-ttu-id="aec3e-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aec3e-119">-InformationAction</span></span>
<span data-ttu-id="aec3e-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="aec3e-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aec3e-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aec3e-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aec3e-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="aec3e-122">Continue</span></span>
- <span data-ttu-id="aec3e-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="aec3e-123">Ignore</span></span>
- <span data-ttu-id="aec3e-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="aec3e-124">Inquire</span></span>
- <span data-ttu-id="aec3e-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aec3e-125">SilentlyContinue</span></span>
- <span data-ttu-id="aec3e-126">állj</span><span class="sxs-lookup"><span data-stu-id="aec3e-126">Stop</span></span>
- <span data-ttu-id="aec3e-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="aec3e-127">Suspend</span></span>

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

### <span data-ttu-id="aec3e-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aec3e-128">-InformationVariable</span></span>
<span data-ttu-id="aec3e-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="aec3e-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aec3e-130">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="aec3e-130">-Launch</span></span>
<span data-ttu-id="aec3e-131">Azt jelzi, hogy ez a parancsmag egy távoli asztali munkamenetet indít a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="aec3e-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec3e-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="aec3e-132">-LocalPath</span></span>
<span data-ttu-id="aec3e-133">A letöltött RDP-fájl teljes elérési útját adja meg a helyi számítógépen.</span><span class="sxs-lookup"><span data-stu-id="aec3e-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec3e-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aec3e-134">-Name</span></span>
<span data-ttu-id="aec3e-135">Azt a virtuális gépet adja meg, amelyre a parancsmag RDP-fájlt tölt le.</span><span class="sxs-lookup"><span data-stu-id="aec3e-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec3e-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="aec3e-136">-Profile</span></span>
<span data-ttu-id="aec3e-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="aec3e-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aec3e-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="aec3e-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aec3e-139">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="aec3e-139">-ServiceName</span></span>
<span data-ttu-id="aec3e-140">Annak az Azure-szolgáltatásnak a nevét adja meg, amelyhez a virtuális gép tartozik.</span><span class="sxs-lookup"><span data-stu-id="aec3e-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="aec3e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec3e-141">CommonParameters</span></span>
<span data-ttu-id="aec3e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aec3e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec3e-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec3e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec3e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aec3e-144">INPUTS</span></span>

## <span data-ttu-id="aec3e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aec3e-145">OUTPUTS</span></span>

## <span data-ttu-id="aec3e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aec3e-146">NOTES</span></span>

## <span data-ttu-id="aec3e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aec3e-147">RELATED LINKS</span></span>

