---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 7bf54ade1d8299c539bd64ad947840b2c97d0d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941833"
---
# <span data-ttu-id="d6fee-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="d6fee-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="d6fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6fee-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fee-103">Törli az Azure IoT-központ tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="d6fee-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="d6fee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6fee-104">SYNTAX</span></span>

### <span data-ttu-id="d6fee-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6fee-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6fee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6fee-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6fee-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fee-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6fee-108">DESCRIPTION</span></span>
<span data-ttu-id="d6fee-109">Az Azure IoT-központban található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát az https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="d6fee-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="d6fee-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6fee-110">EXAMPLES</span></span>

### <span data-ttu-id="d6fee-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d6fee-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="d6fee-112">A MyCertificate törlése</span><span class="sxs-lookup"><span data-stu-id="d6fee-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="d6fee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6fee-113">PARAMETERS</span></span>

### <span data-ttu-id="d6fee-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d6fee-114">-CertificateName</span></span>
<span data-ttu-id="d6fee-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="d6fee-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="d6fee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fee-116">-DefaultProfile</span></span>
<span data-ttu-id="d6fee-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6fee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6fee-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="d6fee-118">-Etag</span></span>
<span data-ttu-id="d6fee-119">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="d6fee-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="d6fee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6fee-120">-InputObject</span></span>
<span data-ttu-id="d6fee-121">Tanúsítványobjektum</span><span class="sxs-lookup"><span data-stu-id="d6fee-121">Certificate Object</span></span>

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

### <span data-ttu-id="d6fee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d6fee-122">-Name</span></span>
<span data-ttu-id="d6fee-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="d6fee-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d6fee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6fee-124">-PassThru</span></span>
<span data-ttu-id="d6fee-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d6fee-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d6fee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fee-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6fee-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d6fee-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6fee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fee-128">-ResourceId</span></span>
<span data-ttu-id="d6fee-129">Tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d6fee-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="d6fee-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6fee-130">-Confirm</span></span>
<span data-ttu-id="d6fee-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6fee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fee-132">-WhatIf</span></span>
<span data-ttu-id="d6fee-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6fee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6fee-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6fee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fee-135">CommonParameters</span></span>
<span data-ttu-id="d6fee-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6fee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fee-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fee-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6fee-138">INPUTS</span></span>

### <span data-ttu-id="d6fee-139">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="d6fee-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="d6fee-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d6fee-140">System.String</span></span>

## <span data-ttu-id="d6fee-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6fee-141">OUTPUTS</span></span>

### <span data-ttu-id="d6fee-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6fee-142">System.Boolean</span></span>

## <span data-ttu-id="d6fee-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6fee-143">NOTES</span></span>

## <span data-ttu-id="d6fee-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6fee-144">RELATED LINKS</span></span>
