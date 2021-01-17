---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478986"
---
# <span data-ttu-id="db9e8-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db9e8-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="db9e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="db9e8-103">A szolgáltatásban háttérkiszolgálóval konfigurált API-kezelési tanúsítványokat kap a közös hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="db9e8-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="db9e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db9e8-104">SYNTAX</span></span>

### <span data-ttu-id="db9e8-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db9e8-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db9e8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9e8-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9e8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db9e8-107">DESCRIPTION</span></span>
<span data-ttu-id="db9e8-108">A **Get-AzApiManagementCertificate parancsmag** az Összes Ön által megadott Azure API Management tanúsítványt vagy tanúsítványt megkapja.</span><span class="sxs-lookup"><span data-stu-id="db9e8-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="db9e8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db9e8-109">EXAMPLES</span></span>

### <span data-ttu-id="db9e8-110">1. példa: Az összes tanúsítvány lekérte</span><span class="sxs-lookup"><span data-stu-id="db9e8-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="db9e8-111">Ez a parancs az összes API-kezelési tanúsítványt beveszi.</span><span class="sxs-lookup"><span data-stu-id="db9e8-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="db9e8-112">2. példa: Tanúsítvány személyazonossága alapján</span><span class="sxs-lookup"><span data-stu-id="db9e8-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="db9e8-113">Ez a parancs a megadott azonosítójú API-kezelési tanúsítványt kapja.</span><span class="sxs-lookup"><span data-stu-id="db9e8-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="db9e8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db9e8-114">PARAMETERS</span></span>

### <span data-ttu-id="db9e8-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="db9e8-115">-CertificateId</span></span>
<span data-ttu-id="db9e8-116">A lekérni szükséges tanúsítvány azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db9e8-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e8-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="db9e8-117">-Context</span></span>
<span data-ttu-id="db9e8-118">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="db9e8-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9e8-119">-DefaultProfile</span></span>
<span data-ttu-id="db9e8-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db9e8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db9e8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db9e8-121">-ResourceId</span></span>
<span data-ttu-id="db9e8-122">A tanúsítvány arm resource identifier.</span><span class="sxs-lookup"><span data-stu-id="db9e8-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="db9e8-123">Ha a megadott érték meg van adva, az azonosító alapján próbálja megtalálni a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="db9e8-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="db9e8-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="db9e8-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db9e8-125">-Confirm</span></span>
<span data-ttu-id="db9e8-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db9e8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9e8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9e8-127">-WhatIf</span></span>
<span data-ttu-id="db9e8-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db9e8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db9e8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db9e8-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9e8-130">CommonParameters</span></span>
<span data-ttu-id="db9e8-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9e8-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db9e8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9e8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db9e8-133">INPUTS</span></span>

### <span data-ttu-id="db9e8-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db9e8-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db9e8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="db9e8-135">System.String</span></span>

## <span data-ttu-id="db9e8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db9e8-136">OUTPUTS</span></span>

### <span data-ttu-id="db9e8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db9e8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="db9e8-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db9e8-138">NOTES</span></span>

## <span data-ttu-id="db9e8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db9e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="db9e8-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db9e8-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="db9e8-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db9e8-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="db9e8-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db9e8-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


