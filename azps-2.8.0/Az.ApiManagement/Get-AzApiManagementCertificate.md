---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 65e9d6783be4814ef4666cfb4dc6405b5004f07e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668117"
---
# <span data-ttu-id="2a3ca-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3ca-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="2a3ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3ca-103">Olyan API-kezelési tanúsítványokat kap, amelyeket a szolgáltatásban a backend szolgáltatással való kölcsönös hitelesítésre konfiguráltak.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="2a3ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a3ca-104">SYNTAX</span></span>

### <span data-ttu-id="2a3ca-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a3ca-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a3ca-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a3ca-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a3ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a3ca-107">DESCRIPTION</span></span>
<span data-ttu-id="2a3ca-108">A **Get-AzApiManagementCertificate** parancsmag minden olyan Azure API-kezelési tanúsítványt vagy tanúsítványt kap, amelyet Ön megadott.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="2a3ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a3ca-109">EXAMPLES</span></span>

### <span data-ttu-id="2a3ca-110">Példa 1: az összes tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a3ca-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="2a3ca-111">Ez a parancs minden API-kezelési tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="2a3ca-112">2. példa: tanúsítvány kérése az AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="2a3ca-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="2a3ca-113">Ez a parancs a megadott AZONOSÍTÓJÚ API-kezelési tanúsítványt kapja.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="2a3ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a3ca-114">PARAMETERS</span></span>

### <span data-ttu-id="2a3ca-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2a3ca-115">-CertificateId</span></span>
<span data-ttu-id="2a3ca-116">A beolvasott tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="2a3ca-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2a3ca-117">-Context</span></span>
<span data-ttu-id="2a3ca-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a3ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3ca-119">-DefaultProfile</span></span>
<span data-ttu-id="2a3ca-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3ca-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a3ca-121">-ResourceId</span></span>
<span data-ttu-id="2a3ca-122">A tanúsítvány ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="2a3ca-123">Ha meg van adva, a program megpróbálja megtalálni a tanúsítványt az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="2a3ca-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-124">This parameter is required.</span></span>

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

### <span data-ttu-id="2a3ca-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a3ca-125">-Confirm</span></span>
<span data-ttu-id="2a3ca-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a3ca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a3ca-127">-WhatIf</span></span>
<span data-ttu-id="2a3ca-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a3ca-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a3ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3ca-130">CommonParameters</span></span>
<span data-ttu-id="2a3ca-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a3ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3ca-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a3ca-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3ca-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a3ca-133">INPUTS</span></span>

### <span data-ttu-id="2a3ca-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a3ca-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a3ca-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2a3ca-135">System.String</span></span>

## <span data-ttu-id="2a3ca-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a3ca-136">OUTPUTS</span></span>

### <span data-ttu-id="2a3ca-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3ca-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="2a3ca-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a3ca-138">NOTES</span></span>

## <span data-ttu-id="2a3ca-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a3ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a3ca-140">Új – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3ca-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="2a3ca-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3ca-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="2a3ca-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3ca-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


