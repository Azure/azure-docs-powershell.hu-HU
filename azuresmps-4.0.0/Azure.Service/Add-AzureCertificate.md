---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016395"
---
# <span data-ttu-id="23043-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23043-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="23043-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23043-102">SYNOPSIS</span></span>
<span data-ttu-id="23043-103">Tanúsítvány feltöltése Azure Cloud-szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="23043-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="23043-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23043-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="23043-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23043-105">DESCRIPTION</span></span>
<span data-ttu-id="23043-106">A **Add-AzureCertificate** parancsmag az Azure-szolgáltatások tanúsítványát tölti fel.</span><span class="sxs-lookup"><span data-stu-id="23043-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="23043-107">Példák</span><span class="sxs-lookup"><span data-stu-id="23043-107">EXAMPLES</span></span>

### <span data-ttu-id="23043-108">1. példa: tanúsítvány és jelszó feltöltése</span><span class="sxs-lookup"><span data-stu-id="23043-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="23043-109">A parancs feltölti a ContosoCertificate. pfx fájlt egy felhőalapú szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="23043-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="23043-110">A parancs a tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23043-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="23043-111">2. példa: tanúsítványfájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="23043-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="23043-112">A parancs feltölti a ContosoCertificate. cer fájlt egy felhőalapú szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="23043-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="23043-113">A parancs a tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23043-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="23043-114">3. példa: a bizonyítvány-objektum feltöltése</span><span class="sxs-lookup"><span data-stu-id="23043-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="23043-115">Az első parancs a Windows PowerShell Core **Get-Item** parancsmag segítségével kap tanúsítványt a felhasználó saját tárolójában.</span><span class="sxs-lookup"><span data-stu-id="23043-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="23043-116">A parancs a $Certificate változóban tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="23043-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="23043-117">A második parancs a $certificate egy felhőalapú szolgáltatásba feltölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="23043-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="23043-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23043-118">PARAMETERS</span></span>

### <span data-ttu-id="23043-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="23043-119">-CertToDeploy</span></span>
<span data-ttu-id="23043-120">A telepítendő tanúsítványt adja meg.</span><span class="sxs-lookup"><span data-stu-id="23043-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="23043-121">Megadhatja a tanúsítványfájl teljes elérési útját, például egy \*. cer vagy \*.</span><span class="sxs-lookup"><span data-stu-id="23043-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="23043-122">pfx-fájlnév-kiterjesztés vagy X. 509 tanúsítvány objektum.</span><span class="sxs-lookup"><span data-stu-id="23043-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23043-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23043-123">-InformationAction</span></span>
<span data-ttu-id="23043-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="23043-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23043-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="23043-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23043-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="23043-126">Continue</span></span>
- <span data-ttu-id="23043-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="23043-127">Ignore</span></span>
- <span data-ttu-id="23043-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="23043-128">Inquire</span></span>
- <span data-ttu-id="23043-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23043-129">SilentlyContinue</span></span>
- <span data-ttu-id="23043-130">állj</span><span class="sxs-lookup"><span data-stu-id="23043-130">Stop</span></span>
- <span data-ttu-id="23043-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="23043-131">Suspend</span></span>

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

### <span data-ttu-id="23043-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23043-132">-InformationVariable</span></span>
<span data-ttu-id="23043-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="23043-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23043-134">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="23043-134">-Password</span></span>
<span data-ttu-id="23043-135">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23043-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23043-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="23043-136">-Profile</span></span>
<span data-ttu-id="23043-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="23043-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23043-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="23043-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23043-139">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="23043-139">-ServiceName</span></span>
<span data-ttu-id="23043-140">Annak az Azure-szolgáltatásnak a nevét adja meg, amelyre a parancsmag hozzáadja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="23043-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

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

### <span data-ttu-id="23043-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23043-141">CommonParameters</span></span>
<span data-ttu-id="23043-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23043-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23043-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23043-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23043-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23043-144">INPUTS</span></span>

## <span data-ttu-id="23043-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23043-145">OUTPUTS</span></span>

### <span data-ttu-id="23043-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="23043-146">ManagementOperationContext</span></span>

## <span data-ttu-id="23043-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23043-147">NOTES</span></span>

## <span data-ttu-id="23043-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23043-148">RELATED LINKS</span></span>

[<span data-ttu-id="23043-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23043-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="23043-150">Új – AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="23043-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="23043-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23043-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


