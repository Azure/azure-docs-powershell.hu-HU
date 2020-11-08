---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015982"
---
# <span data-ttu-id="3b34a-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="3b34a-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="3b34a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b34a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b34a-103">A meglévő tanúsítvány új, Linux-alapú Azure virtuális gépre való beszúrására szolgáló SSH-kulcs objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3b34a-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="3b34a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b34a-104">SYNTAX</span></span>

### <span data-ttu-id="3b34a-105">kulcspár</span><span class="sxs-lookup"><span data-stu-id="3b34a-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3b34a-106">PUBLICKEY</span><span class="sxs-lookup"><span data-stu-id="3b34a-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b34a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b34a-107">DESCRIPTION</span></span>
<span data-ttu-id="3b34a-108">A **New-AzureSSHKey** parancsmag létrehoz egy SSH-kulcsú objektumot egy olyan tanúsítványhoz, amely már hozzá lett adva az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="3b34a-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="3b34a-109">Ezt az SSH billentyűt ezt követően az új **AzureProvisioningConfig** is használhatja, ha új virtuális gépet hoz létre a konfigurációs objektumhoz új **AzureVM** , vagy ha új virtuális gépet hoz létre a **New-AzureQuickVM** használatával.</span><span class="sxs-lookup"><span data-stu-id="3b34a-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="3b34a-110">Ha a virtuálisgép-készítő parancsfájlok részeként része, akkor a megadott SSH nyilvános kulcsot vagy kulcspárt adja hozzá az új virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="3b34a-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="3b34a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3b34a-111">EXAMPLES</span></span>

### <span data-ttu-id="3b34a-112">Példa 1: tanúsítvány-beállítási objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b34a-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="3b34a-113">Ez a parancs létrehoz egy tanúsítvány-beállítási objektumot egy meglévő tanúsítványhoz, majd egy változóban tárolja az objektumot későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="3b34a-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="3b34a-114">2. példa: tanúsítvány felvétele szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="3b34a-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="3b34a-115">Ez a parancs tanúsítványokat ad egy Azure-szolgáltatáshoz, majd létrehoz egy új, a tanúsítványt használó virtuális virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="3b34a-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="3b34a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b34a-116">PARAMETERS</span></span>

### <span data-ttu-id="3b34a-117">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="3b34a-117">-Fingerprint</span></span>
<span data-ttu-id="3b34a-118">A tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b34a-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="3b34a-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b34a-119">-InformationAction</span></span>
<span data-ttu-id="3b34a-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3b34a-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b34a-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3b34a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b34a-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3b34a-122">Continue</span></span>
- <span data-ttu-id="3b34a-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3b34a-123">Ignore</span></span>
- <span data-ttu-id="3b34a-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3b34a-124">Inquire</span></span>
- <span data-ttu-id="3b34a-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b34a-125">SilentlyContinue</span></span>
- <span data-ttu-id="3b34a-126">állj</span><span class="sxs-lookup"><span data-stu-id="3b34a-126">Stop</span></span>
- <span data-ttu-id="3b34a-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3b34a-127">Suspend</span></span>

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

### <span data-ttu-id="3b34a-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b34a-128">-InformationVariable</span></span>
<span data-ttu-id="3b34a-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3b34a-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b34a-130">-Kulcspár</span><span class="sxs-lookup"><span data-stu-id="3b34a-130">-KeyPair</span></span>
<span data-ttu-id="3b34a-131">Itt adhatja meg, hogy ez a parancsmag létrehoz egy olyan objektumot, amely egy SSH kulcspár beszúrását az új virtuálisgép-konfigurációba illeszti be.</span><span class="sxs-lookup"><span data-stu-id="3b34a-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b34a-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3b34a-132">-Path</span></span>
<span data-ttu-id="3b34a-133">Az SSH-beli nyilvános kulcs vagy kulcspár tárolásának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b34a-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b34a-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="3b34a-134">-PublicKey</span></span>
<span data-ttu-id="3b34a-135">Itt adhatja meg, hogy a parancsmag létrehoz egy olyan objektumot, amely egy SSH nyilvános kulcs beszúrását az új virtuálisgép-konfigurációba illeszti be.</span><span class="sxs-lookup"><span data-stu-id="3b34a-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b34a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b34a-136">CommonParameters</span></span>
<span data-ttu-id="3b34a-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b34a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b34a-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b34a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b34a-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b34a-139">INPUTS</span></span>

## <span data-ttu-id="3b34a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b34a-140">OUTPUTS</span></span>

## <span data-ttu-id="3b34a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b34a-141">NOTES</span></span>

## <span data-ttu-id="3b34a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b34a-142">RELATED LINKS</span></span>

[<span data-ttu-id="3b34a-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="3b34a-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="3b34a-144">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="3b34a-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="3b34a-145">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="3b34a-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="3b34a-146">Új – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="3b34a-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


