---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
ms.openlocfilehash: b38fd64db24a38267b3d06d8046f1bcbb826537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673053"
---
# <span data-ttu-id="8bccd-101">Add-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="8bccd-101">Add-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="8bccd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bccd-102">SYNOPSIS</span></span>
<span data-ttu-id="8bccd-103">Azure IoT hub tanúsítvány létrehozása/frissítése</span><span class="sxs-lookup"><span data-stu-id="8bccd-103">Create/update an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bccd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bccd-104">SYNTAX</span></span>

### <span data-ttu-id="8bccd-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8bccd-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bccd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bccd-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bccd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bccd-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bccd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bccd-108">DESCRIPTION</span></span>
<span data-ttu-id="8bccd-109">Új tanúsítvány feltöltése vagy a meglévő tanúsítvány cseréje ugyanazzal a névvel.</span><span class="sxs-lookup"><span data-stu-id="8bccd-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="8bccd-110">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="8bccd-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="8bccd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8bccd-111">EXAMPLES</span></span>

### <span data-ttu-id="8bccd-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8bccd-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="8bccd-113">Egy HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány CER-fájlt tölt fel egy IoT-hub-ra.</span><span class="sxs-lookup"><span data-stu-id="8bccd-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="8bccd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8bccd-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="8bccd-115">Egy új CER-fájl feltöltésével frissíti a HITELESÍTÉSSZOLGÁLTATÓI tanúsítványt egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="8bccd-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="8bccd-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bccd-116">PARAMETERS</span></span>

### <span data-ttu-id="8bccd-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8bccd-117">-CertificateName</span></span>
<span data-ttu-id="8bccd-118">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="8bccd-118">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bccd-119">-DefaultProfile</span></span>
<span data-ttu-id="8bccd-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bccd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-121">-ETAG</span><span class="sxs-lookup"><span data-stu-id="8bccd-121">-Etag</span></span>
<span data-ttu-id="8bccd-122">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="8bccd-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8bccd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bccd-123">-InputObject</span></span>
<span data-ttu-id="8bccd-124">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="8bccd-124">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8bccd-125">-Name</span></span>
<span data-ttu-id="8bccd-126">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="8bccd-126">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8bccd-127">-Path</span></span>
<span data-ttu-id="8bccd-128">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="8bccd-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="8bccd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bccd-129">-ResourceGroupName</span></span>
<span data-ttu-id="8bccd-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8bccd-130">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bccd-131">-ResourceId</span></span>
<span data-ttu-id="8bccd-132">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="8bccd-132">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bccd-133">-Confirm</span></span>
<span data-ttu-id="8bccd-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bccd-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bccd-135">-WhatIf</span></span>
<span data-ttu-id="8bccd-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bccd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bccd-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bccd-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bccd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bccd-138">CommonParameters</span></span>
<span data-ttu-id="8bccd-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bccd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bccd-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bccd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bccd-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bccd-141">INPUTS</span></span>

### <span data-ttu-id="8bccd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8bccd-142">System.String</span></span>

## <span data-ttu-id="8bccd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bccd-143">OUTPUTS</span></span>

### <span data-ttu-id="8bccd-144">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="8bccd-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="8bccd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bccd-145">NOTES</span></span>

## <span data-ttu-id="8bccd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bccd-146">RELATED LINKS</span></span>

