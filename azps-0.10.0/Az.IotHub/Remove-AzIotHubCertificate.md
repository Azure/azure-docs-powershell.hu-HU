---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 94df7d1870577711174dc4f810c74af528256cb0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842210"
---
# <span data-ttu-id="9a3e5-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="9a3e5-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="9a3e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3e5-103">Azure IoT hub tanúsítvány törlése</span><span class="sxs-lookup"><span data-stu-id="9a3e5-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="9a3e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a3e5-104">SYNTAX</span></span>

### <span data-ttu-id="9a3e5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a3e5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a3e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9a3e5-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a3e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9a3e5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a3e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="9a3e5-109">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="9a3e5-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="9a3e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9a3e5-110">EXAMPLES</span></span>

### <span data-ttu-id="9a3e5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a3e5-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="9a3e5-112">MyCertificate törlése</span><span class="sxs-lookup"><span data-stu-id="9a3e5-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="9a3e5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a3e5-113">PARAMETERS</span></span>

### <span data-ttu-id="9a3e5-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9a3e5-114">-CertificateName</span></span>
<span data-ttu-id="9a3e5-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="9a3e5-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="9a3e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3e5-116">-DefaultProfile</span></span>
<span data-ttu-id="9a3e5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a3e5-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="9a3e5-118">-Etag</span></span>
<span data-ttu-id="9a3e5-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="9a3e5-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9a3e5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a3e5-120">-InputObject</span></span>
<span data-ttu-id="9a3e5-121">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="9a3e5-121">Certificate Object</span></span>

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

### <span data-ttu-id="9a3e5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a3e5-122">-Name</span></span>
<span data-ttu-id="9a3e5-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="9a3e5-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9a3e5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a3e5-124">-PassThru</span></span>
<span data-ttu-id="9a3e5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9a3e5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9a3e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a3e5-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9a3e5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9a3e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a3e5-128">-ResourceId</span></span>
<span data-ttu-id="9a3e5-129">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="9a3e5-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="9a3e5-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a3e5-130">-Confirm</span></span>
<span data-ttu-id="9a3e5-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a3e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a3e5-132">-WhatIf</span></span>
<span data-ttu-id="9a3e5-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a3e5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a3e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3e5-135">CommonParameters</span></span>
<span data-ttu-id="9a3e5-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a3e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3e5-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3e5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3e5-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a3e5-138">INPUTS</span></span>

### <span data-ttu-id="9a3e5-139">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="9a3e5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="9a3e5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9a3e5-140">System.String</span></span>

## <span data-ttu-id="9a3e5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a3e5-141">OUTPUTS</span></span>

### <span data-ttu-id="9a3e5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a3e5-142">System.Boolean</span></span>

## <span data-ttu-id="9a3e5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a3e5-143">NOTES</span></span>

## <span data-ttu-id="9a3e5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a3e5-144">RELATED LINKS</span></span>
