---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495345"
---
# <span data-ttu-id="eacaa-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="eacaa-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="eacaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eacaa-102">SYNOPSIS</span></span>
<span data-ttu-id="eacaa-103">Azure IoT hub tanúsítvány törlése</span><span class="sxs-lookup"><span data-stu-id="eacaa-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eacaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eacaa-104">SYNTAX</span></span>

### <span data-ttu-id="eacaa-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eacaa-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eacaa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eacaa-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eacaa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eacaa-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eacaa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eacaa-108">DESCRIPTION</span></span>
<span data-ttu-id="eacaa-109">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="eacaa-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="eacaa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eacaa-110">EXAMPLES</span></span>

### <span data-ttu-id="eacaa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eacaa-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="eacaa-112">MyCertificate törlése</span><span class="sxs-lookup"><span data-stu-id="eacaa-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="eacaa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eacaa-113">PARAMETERS</span></span>

### <span data-ttu-id="eacaa-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="eacaa-114">-CertificateName</span></span>
<span data-ttu-id="eacaa-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="eacaa-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="eacaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eacaa-116">-DefaultProfile</span></span>
<span data-ttu-id="eacaa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eacaa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eacaa-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="eacaa-118">-Etag</span></span>
<span data-ttu-id="eacaa-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="eacaa-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacaa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eacaa-120">-InputObject</span></span>
<span data-ttu-id="eacaa-121">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="eacaa-121">Certificate Object</span></span>

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

### <span data-ttu-id="eacaa-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eacaa-122">-Name</span></span>
<span data-ttu-id="eacaa-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="eacaa-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="eacaa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eacaa-124">-PassThru</span></span>
<span data-ttu-id="eacaa-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eacaa-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacaa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eacaa-126">-ResourceGroupName</span></span>
<span data-ttu-id="eacaa-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eacaa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="eacaa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eacaa-128">-ResourceId</span></span>
<span data-ttu-id="eacaa-129">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="eacaa-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="eacaa-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eacaa-130">-Confirm</span></span>
<span data-ttu-id="eacaa-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eacaa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eacaa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eacaa-132">-WhatIf</span></span>
<span data-ttu-id="eacaa-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eacaa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eacaa-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eacaa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eacaa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacaa-135">CommonParameters</span></span>
<span data-ttu-id="eacaa-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eacaa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eacaa-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eacaa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacaa-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eacaa-138">INPUTS</span></span>

### <span data-ttu-id="eacaa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eacaa-139">System.String</span></span>

## <span data-ttu-id="eacaa-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eacaa-140">OUTPUTS</span></span>

### <span data-ttu-id="eacaa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eacaa-141">System.Boolean</span></span>

## <span data-ttu-id="eacaa-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eacaa-142">NOTES</span></span>

## <span data-ttu-id="eacaa-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eacaa-143">RELATED LINKS</span></span>

