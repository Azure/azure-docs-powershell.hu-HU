---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016167"
---
# <span data-ttu-id="9255a-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9255a-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="9255a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9255a-102">SYNOPSIS</span></span>
<span data-ttu-id="9255a-103">Tanúsítvány eltávolítása Azure-szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="9255a-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="9255a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9255a-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9255a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9255a-105">DESCRIPTION</span></span>
<span data-ttu-id="9255a-106">A **Remove-AzureCertificate** parancsmag az Azure-szolgáltatások tanúsítványait távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9255a-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="9255a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9255a-107">EXAMPLES</span></span>

### <span data-ttu-id="9255a-108">1. példa: tanúsítvány eltávolítása egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="9255a-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="9255a-109">Ez a parancs eltávolítja azt a tanúsítvány-objektumot, amely a Felhőbeli szolgáltatás megadott ujjlenyomatával rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="9255a-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="9255a-110">2. példa: az összes tanúsítvány eltávolítása egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="9255a-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="9255a-111">Ez a parancs a **Get-AzureCertificate** parancsmag használatával kapja meg a ContosoService nevű szolgáltatás összes tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="9255a-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="9255a-112">A parancs a csővezeték-kezelő segítségével átadja az egyes tanúsítványokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9255a-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9255a-113">Ez a parancsmag eltávolítja az egyes tanúsítványokat a felhőalapú szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="9255a-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="9255a-114">3. példa: egy adott ujjlenyomat-algoritmust használó szolgáltatás összes tanúsítványának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9255a-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="9255a-115">Ez a parancs a ContosoService nevű szolgáltatás összes olyan tanúsítványát beolvassa, amely az SHA1 ujjlenyomat-algoritmust használja.</span><span class="sxs-lookup"><span data-stu-id="9255a-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="9255a-116">A parancs átadja az egyes tanúsítványokat az aktuális parancsmagnak, amely az egyes tanúsítványokat eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9255a-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="9255a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9255a-117">PARAMETERS</span></span>

### <span data-ttu-id="9255a-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9255a-118">-InformationAction</span></span>
<span data-ttu-id="9255a-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="9255a-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9255a-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9255a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9255a-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="9255a-121">Continue</span></span>
- <span data-ttu-id="9255a-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="9255a-122">Ignore</span></span>
- <span data-ttu-id="9255a-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="9255a-123">Inquire</span></span>
- <span data-ttu-id="9255a-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9255a-124">SilentlyContinue</span></span>
- <span data-ttu-id="9255a-125">állj</span><span class="sxs-lookup"><span data-stu-id="9255a-125">Stop</span></span>
- <span data-ttu-id="9255a-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="9255a-126">Suspend</span></span>

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

### <span data-ttu-id="9255a-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9255a-127">-InformationVariable</span></span>
<span data-ttu-id="9255a-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="9255a-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9255a-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="9255a-129">-Profile</span></span>
<span data-ttu-id="9255a-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9255a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9255a-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9255a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9255a-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="9255a-132">-ServiceName</span></span>
<span data-ttu-id="9255a-133">Annak az Azure-szolgáltatásnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9255a-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="9255a-134">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="9255a-134">-Thumbprint</span></span>
<span data-ttu-id="9255a-135">A parancsmag által eltávolított tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9255a-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9255a-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9255a-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9255a-137">A tanúsítvány ujjlenyomatának létrehozásához használt algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="9255a-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

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

### <span data-ttu-id="9255a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9255a-138">CommonParameters</span></span>
<span data-ttu-id="9255a-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9255a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9255a-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9255a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9255a-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9255a-141">INPUTS</span></span>

## <span data-ttu-id="9255a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9255a-142">OUTPUTS</span></span>

### <span data-ttu-id="9255a-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="9255a-143">ManagementOperationContext</span></span>

## <span data-ttu-id="9255a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9255a-144">NOTES</span></span>

## <span data-ttu-id="9255a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9255a-145">RELATED LINKS</span></span>

[<span data-ttu-id="9255a-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9255a-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="9255a-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9255a-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="9255a-148">Új – AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="9255a-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


