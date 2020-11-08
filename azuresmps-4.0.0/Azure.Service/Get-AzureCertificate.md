---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016356"
---
# <span data-ttu-id="408d2-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="408d2-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="408d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="408d2-102">SYNOPSIS</span></span>
<span data-ttu-id="408d2-103">Egy tanúsítvány-objektumot kap egy Azure-szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="408d2-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="408d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="408d2-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="408d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="408d2-105">DESCRIPTION</span></span>
<span data-ttu-id="408d2-106">A **Get-AzureCertificate** parancsmag az Azure-szolgáltatásból kapja meg a tanúsítvány objektumát.</span><span class="sxs-lookup"><span data-stu-id="408d2-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="408d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="408d2-107">EXAMPLES</span></span>

### <span data-ttu-id="408d2-108">Példa 1: tanúsítvány beszerzése egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="408d2-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="408d2-109">Ez a parancs a ContosoService nevű szolgáltatásból kapja a tanúsítványok objektumait, majd a $AzureCert változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="408d2-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="408d2-110">2. példa: tanúsítvány beszerzése egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="408d2-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="408d2-111">Ez a parancs a ContosoService nevű szolgáltatás által megadott ujjlenyomat által meghatározott tanúsítvány-objektumot kapja, majd a $AzureCert változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="408d2-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="408d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="408d2-112">PARAMETERS</span></span>

### <span data-ttu-id="408d2-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="408d2-113">-InformationAction</span></span>
<span data-ttu-id="408d2-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="408d2-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="408d2-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="408d2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="408d2-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="408d2-116">Continue</span></span>
- <span data-ttu-id="408d2-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="408d2-117">Ignore</span></span>
- <span data-ttu-id="408d2-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="408d2-118">Inquire</span></span>
- <span data-ttu-id="408d2-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="408d2-119">SilentlyContinue</span></span>
- <span data-ttu-id="408d2-120">állj</span><span class="sxs-lookup"><span data-stu-id="408d2-120">Stop</span></span>
- <span data-ttu-id="408d2-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="408d2-121">Suspend</span></span>

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

### <span data-ttu-id="408d2-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="408d2-122">-InformationVariable</span></span>
<span data-ttu-id="408d2-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="408d2-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="408d2-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="408d2-124">-Profile</span></span>
<span data-ttu-id="408d2-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="408d2-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="408d2-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="408d2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="408d2-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="408d2-127">-ServiceName</span></span>
<span data-ttu-id="408d2-128">Annak az Azure-szolgáltatásnak a nevét adja meg, amelyből a parancsmag tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="408d2-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

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

### <span data-ttu-id="408d2-129">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="408d2-129">-Thumbprint</span></span>
<span data-ttu-id="408d2-130">Annak a tanúsítványnak az ujjlenyomatát adja meg, amely az adott parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="408d2-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408d2-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="408d2-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="408d2-132">A tanúsítvány ujjlenyomatának létrehozásához használt algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="408d2-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408d2-133">CommonParameters</span></span>
<span data-ttu-id="408d2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="408d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408d2-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408d2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="408d2-136">INPUTS</span></span>

## <span data-ttu-id="408d2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="408d2-137">OUTPUTS</span></span>

### <span data-ttu-id="408d2-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="408d2-138">CertificateContext</span></span>

## <span data-ttu-id="408d2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="408d2-139">NOTES</span></span>

## <span data-ttu-id="408d2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="408d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="408d2-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="408d2-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="408d2-142">Új – AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="408d2-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="408d2-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="408d2-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


