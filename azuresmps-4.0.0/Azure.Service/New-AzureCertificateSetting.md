---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015932"
---
# <span data-ttu-id="477ef-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="477ef-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="477ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="477ef-102">SYNOPSIS</span></span>
<span data-ttu-id="477ef-103">Tanúsítvány-beállítási objektum létrehozása egy szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="477ef-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="477ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="477ef-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="477ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="477ef-105">DESCRIPTION</span></span>
<span data-ttu-id="477ef-106">A **New-AzureCertificateSetting** parancsmag létrehoz egy tanúsítvány-beállítási objektumot egy Azure-szolgáltatásban található tanúsítványhoz.</span><span class="sxs-lookup"><span data-stu-id="477ef-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="477ef-107">Az **Add-AzureProvisioningConfig** parancsmaggal egy tanúsítvány-beállítási objektum segítségével hozhat létre konfigurációs objektumokat.</span><span class="sxs-lookup"><span data-stu-id="477ef-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="477ef-108">A **New-AzureVM** parancsmaggal virtuális gépet hozhat létre a konfigurációs objektumokkal.</span><span class="sxs-lookup"><span data-stu-id="477ef-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="477ef-109">A tanúsítvány-beállítási objektum segítségével virtuális gépet hozhat létre a **New-AzureQuickVM** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="477ef-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="477ef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="477ef-110">EXAMPLES</span></span>

### <span data-ttu-id="477ef-111">Példa 1: tanúsítvány-beállítási objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="477ef-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="477ef-112">Ezzel a paranccsal létrehoz egy tanúsítvány-beállítási objektumot egy meglévő tanúsítványhoz.</span><span class="sxs-lookup"><span data-stu-id="477ef-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="477ef-113">2. példa: konfigurációs beállítási objektumot használó virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="477ef-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="477ef-114">Az első parancs az **Add-AzureCertificate** parancsmag segítségével hozzáadja a ContosoCert. cer nevű tanúsítványt a ContosoService nevű szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="477ef-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="477ef-115">A második parancs létrehozza a tanúsítvány-beállítási objektumot, majd a $CertificateSetting változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="477ef-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="477ef-116">A harmadik parancs a **Get-AzureVMImage** parancsmag segítségével kap képet a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="477ef-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="477ef-117">Ez a parancs a képet a $Image változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="477ef-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="477ef-118">A végleges parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag segítségével hozza létre a $image kép alapján.</span><span class="sxs-lookup"><span data-stu-id="477ef-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="477ef-119">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az **Add-AzureProvisioningConfig** parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="477ef-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="477ef-120">Ebben a parancsmagban kiépítési adatok adhatók hozzá a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="477ef-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="477ef-121">A parancs átadja az objektumot a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="477ef-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="477ef-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="477ef-122">PARAMETERS</span></span>

### <span data-ttu-id="477ef-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="477ef-123">-InformationAction</span></span>
<span data-ttu-id="477ef-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="477ef-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="477ef-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="477ef-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="477ef-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="477ef-126">Continue</span></span>
- <span data-ttu-id="477ef-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="477ef-127">Ignore</span></span>
- <span data-ttu-id="477ef-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="477ef-128">Inquire</span></span>
- <span data-ttu-id="477ef-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="477ef-129">SilentlyContinue</span></span>
- <span data-ttu-id="477ef-130">állj</span><span class="sxs-lookup"><span data-stu-id="477ef-130">Stop</span></span>
- <span data-ttu-id="477ef-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="477ef-131">Suspend</span></span>

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

### <span data-ttu-id="477ef-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="477ef-132">-InformationVariable</span></span>
<span data-ttu-id="477ef-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="477ef-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="477ef-134">-StoreName mezőt</span><span class="sxs-lookup"><span data-stu-id="477ef-134">-StoreName</span></span>
<span data-ttu-id="477ef-135">Azt a tanúsítványtárolót adja meg, amelybe a tanúsítványt be szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="477ef-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="477ef-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="477ef-136">Valid values are:</span></span> 

- <span data-ttu-id="477ef-137">AddressBook</span><span class="sxs-lookup"><span data-stu-id="477ef-137">AddressBook</span></span>
- <span data-ttu-id="477ef-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="477ef-138">AuthRoot</span></span>
- <span data-ttu-id="477ef-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="477ef-139">CertificateAuthority</span></span>
- <span data-ttu-id="477ef-140">Fájltípusa nem engedélyezett</span><span class="sxs-lookup"><span data-stu-id="477ef-140">Disallowed</span></span>
- <span data-ttu-id="477ef-141">A</span><span class="sxs-lookup"><span data-stu-id="477ef-141">My</span></span>
- <span data-ttu-id="477ef-142">Legfelső szintű</span><span class="sxs-lookup"><span data-stu-id="477ef-142">Root</span></span>
- <span data-ttu-id="477ef-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="477ef-143">TrustedPeople</span></span>
- <span data-ttu-id="477ef-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="477ef-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477ef-145">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="477ef-145">-Thumbprint</span></span>
<span data-ttu-id="477ef-146">A tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="477ef-146">Specifies the thumbprint of the certificate.</span></span>

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

### <span data-ttu-id="477ef-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477ef-147">CommonParameters</span></span>
<span data-ttu-id="477ef-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="477ef-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477ef-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477ef-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477ef-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="477ef-150">INPUTS</span></span>

## <span data-ttu-id="477ef-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="477ef-151">OUTPUTS</span></span>

## <span data-ttu-id="477ef-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="477ef-152">NOTES</span></span>

## <span data-ttu-id="477ef-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="477ef-153">RELATED LINKS</span></span>

[<span data-ttu-id="477ef-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="477ef-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="477ef-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="477ef-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="477ef-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="477ef-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="477ef-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="477ef-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="477ef-158">Új – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="477ef-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="477ef-159">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="477ef-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="477ef-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="477ef-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


