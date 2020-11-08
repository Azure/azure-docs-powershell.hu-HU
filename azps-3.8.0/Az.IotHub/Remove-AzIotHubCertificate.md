---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013800"
---
# <span data-ttu-id="7198d-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="7198d-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="7198d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7198d-102">SYNOPSIS</span></span>
<span data-ttu-id="7198d-103">Azure IoT hub tanúsítvány törlése</span><span class="sxs-lookup"><span data-stu-id="7198d-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="7198d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7198d-104">SYNTAX</span></span>

### <span data-ttu-id="7198d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7198d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7198d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7198d-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7198d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7198d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7198d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7198d-108">DESCRIPTION</span></span>
<span data-ttu-id="7198d-109">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="7198d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="7198d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7198d-110">EXAMPLES</span></span>

### <span data-ttu-id="7198d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7198d-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="7198d-112">MyCertificate törlése</span><span class="sxs-lookup"><span data-stu-id="7198d-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="7198d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7198d-113">PARAMETERS</span></span>

### <span data-ttu-id="7198d-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7198d-114">-CertificateName</span></span>
<span data-ttu-id="7198d-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="7198d-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7198d-116">-DefaultProfile</span></span>
<span data-ttu-id="7198d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7198d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="7198d-118">-Etag</span></span>
<span data-ttu-id="7198d-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="7198d-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7198d-120">-InputObject</span></span>
<span data-ttu-id="7198d-121">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="7198d-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7198d-122">-Name</span></span>
<span data-ttu-id="7198d-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="7198d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7198d-124">-PassThru</span></span>
<span data-ttu-id="7198d-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7198d-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7198d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7198d-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7198d-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7198d-128">-ResourceId</span></span>
<span data-ttu-id="7198d-129">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="7198d-129">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7198d-130">-Confirm</span></span>
<span data-ttu-id="7198d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7198d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7198d-132">-WhatIf</span></span>
<span data-ttu-id="7198d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7198d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7198d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7198d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7198d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7198d-135">CommonParameters</span></span>
<span data-ttu-id="7198d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7198d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7198d-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7198d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7198d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7198d-138">INPUTS</span></span>

### <span data-ttu-id="7198d-139">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="7198d-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="7198d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7198d-140">System.String</span></span>

## <span data-ttu-id="7198d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7198d-141">OUTPUTS</span></span>

### <span data-ttu-id="7198d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7198d-142">System.Boolean</span></span>

## <span data-ttu-id="7198d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7198d-143">NOTES</span></span>

## <span data-ttu-id="7198d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7198d-144">RELATED LINKS</span></span>
