---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015955"
---
# <span data-ttu-id="530ad-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="530ad-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="530ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="530ad-102">SYNOPSIS</span></span>
<span data-ttu-id="530ad-103">Nyilvános IP-címet ad az Azure Virtual Machine-nek.</span><span class="sxs-lookup"><span data-stu-id="530ad-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="530ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="530ad-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="530ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="530ad-105">DESCRIPTION</span></span>
<span data-ttu-id="530ad-106">A **set-AzurePublicIP** parancsmag nyilvános IP-címet ad egy Azure Virtual Machine-nek.</span><span class="sxs-lookup"><span data-stu-id="530ad-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="530ad-107">Ha egy meglévő virtuális géphez futtatja ezt a parancsmagot, frissítse a virtuális gépet a módosítások végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="530ad-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="530ad-108">Megadhat egy tartománynév-címkét, amely a nyilvános IP-hez megfelelő DNS-bejegyzést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="530ad-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="530ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="530ad-109">EXAMPLES</span></span>

### <span data-ttu-id="530ad-110">1. példa: nyilvános IP-cím hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="530ad-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="530ad-111">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="530ad-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="530ad-112">A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="530ad-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="530ad-113">Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip.</span><span class="sxs-lookup"><span data-stu-id="530ad-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="530ad-114">A parancs átadja a virtuális gépet az **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="530ad-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="530ad-115">2. példa: nyilvános IP hozzáadása egy új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="530ad-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="530ad-116">Ez a parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag használatával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="530ad-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="530ad-117">A parancs átadja az objektumot az **Add-AzureProvisioningConfig** parancsmagnak, ami további konfigurációt biztosít.</span><span class="sxs-lookup"><span data-stu-id="530ad-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="530ad-118">Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip.</span><span class="sxs-lookup"><span data-stu-id="530ad-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="530ad-119">A parancs átadja a konfigurációt a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="530ad-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="530ad-120">3. példa: nyilvános IP-cím és címke hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="530ad-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="530ad-121">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="530ad-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="530ad-122">A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="530ad-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="530ad-123">Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip és a címke ipname.</span><span class="sxs-lookup"><span data-stu-id="530ad-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="530ad-124">A parancs frissíti a virtuális gépet, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="530ad-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="530ad-125">4. példa: nyilvános IP-cím és címke hozzáadása egy új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="530ad-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="530ad-126">Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az objektumot a **AzureProvisioningConfig** , amely további konfigurációt biztosít.</span><span class="sxs-lookup"><span data-stu-id="530ad-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="530ad-127">Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip és a címke ipname.</span><span class="sxs-lookup"><span data-stu-id="530ad-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="530ad-128">A parancs a virtuális gépet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="530ad-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="530ad-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="530ad-129">PARAMETERS</span></span>

### <span data-ttu-id="530ad-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="530ad-130">-DomainNameLabel</span></span>
<span data-ttu-id="530ad-131">Adja meg a nyilvános IP-címhez tartozó DNS-bejegyzéshez használni kívánt nevet.</span><span class="sxs-lookup"><span data-stu-id="530ad-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="530ad-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="530ad-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="530ad-133">A TCP üresjárati időtúllépési időszakát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="530ad-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="530ad-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="530ad-134">-InformationAction</span></span>
<span data-ttu-id="530ad-135">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="530ad-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="530ad-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="530ad-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="530ad-137">Folytassa</span><span class="sxs-lookup"><span data-stu-id="530ad-137">Continue</span></span>
- <span data-ttu-id="530ad-138">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="530ad-138">Ignore</span></span>
- <span data-ttu-id="530ad-139">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="530ad-139">Inquire</span></span>
- <span data-ttu-id="530ad-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="530ad-140">SilentlyContinue</span></span>
- <span data-ttu-id="530ad-141">állj</span><span class="sxs-lookup"><span data-stu-id="530ad-141">Stop</span></span>
- <span data-ttu-id="530ad-142">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="530ad-142">Suspend</span></span>

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

### <span data-ttu-id="530ad-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="530ad-143">-InformationVariable</span></span>
<span data-ttu-id="530ad-144">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="530ad-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="530ad-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="530ad-145">-Profile</span></span>
<span data-ttu-id="530ad-146">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="530ad-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="530ad-147">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="530ad-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="530ad-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="530ad-148">-PublicIPName</span></span>
<span data-ttu-id="530ad-149">Adja meg a nyilvános IP-nevet.</span><span class="sxs-lookup"><span data-stu-id="530ad-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="530ad-150">-VM</span><span class="sxs-lookup"><span data-stu-id="530ad-150">-VM</span></span>
<span data-ttu-id="530ad-151">Azt a virtuális gépet adja meg, amelyre a parancsmag hozzáadja a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="530ad-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

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

### <span data-ttu-id="530ad-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530ad-152">CommonParameters</span></span>
<span data-ttu-id="530ad-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="530ad-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530ad-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="530ad-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530ad-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="530ad-155">INPUTS</span></span>

## <span data-ttu-id="530ad-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="530ad-156">OUTPUTS</span></span>

### <span data-ttu-id="530ad-157">Microsoft. WindowsAzure. Command. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="530ad-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="530ad-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="530ad-158">NOTES</span></span>

## <span data-ttu-id="530ad-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="530ad-159">RELATED LINKS</span></span>

[<span data-ttu-id="530ad-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="530ad-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="530ad-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="530ad-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="530ad-162">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="530ad-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="530ad-163">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="530ad-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="530ad-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="530ad-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="530ad-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="530ad-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


