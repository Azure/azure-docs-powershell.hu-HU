---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: b6825d23244664b475dbd28472dc30f33117a59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678997"
---
# <span data-ttu-id="6b894-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6b894-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="6b894-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b894-102">SYNOPSIS</span></span>
<span data-ttu-id="6b894-103">Olyan API-kezelési tanúsítványokat kap, amelyeket a szolgáltatásban a backend szolgáltatással való kölcsönös hitelesítésre konfiguráltak.</span><span class="sxs-lookup"><span data-stu-id="6b894-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b894-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b894-104">SYNTAX</span></span>

### <span data-ttu-id="6b894-105">GetAllCertificates (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b894-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b894-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="6b894-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b894-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b894-107">DESCRIPTION</span></span>
<span data-ttu-id="6b894-108">A **Get-AzureRmApiManagementCertificate** parancsmag minden olyan Azure API-kezelési tanúsítványt vagy tanúsítványt kap, amelyet Ön megadott.</span><span class="sxs-lookup"><span data-stu-id="6b894-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="6b894-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b894-109">EXAMPLES</span></span>

### <span data-ttu-id="6b894-110">Példa 1: az összes tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="6b894-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="6b894-111">Ez a parancs minden API-kezelési tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="6b894-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="6b894-112">2. példa: tanúsítvány kérése az AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6b894-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="6b894-113">Ez a parancs a megadott AZONOSÍTÓJÚ API-kezelési tanúsítványt kapja.</span><span class="sxs-lookup"><span data-stu-id="6b894-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="6b894-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b894-114">PARAMETERS</span></span>

### <span data-ttu-id="6b894-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="6b894-115">-CertificateId</span></span>
<span data-ttu-id="6b894-116">A beolvasott tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b894-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByCertificateId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b894-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6b894-117">-Context</span></span>
<span data-ttu-id="6b894-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b894-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b894-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b894-119">-DefaultProfile</span></span>
<span data-ttu-id="6b894-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b894-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6b894-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b894-121">-Confirm</span></span>
<span data-ttu-id="6b894-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b894-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b894-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b894-123">-WhatIf</span></span>
<span data-ttu-id="6b894-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b894-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b894-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b894-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b894-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b894-126">CommonParameters</span></span>
<span data-ttu-id="6b894-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b894-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b894-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b894-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b894-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b894-129">INPUTS</span></span>

### <span data-ttu-id="6b894-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b894-130">None</span></span>
<span data-ttu-id="6b894-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6b894-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b894-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b894-132">OUTPUTS</span></span>

### <span data-ttu-id="6b894-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6b894-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="6b894-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b894-134">NOTES</span></span>

## <span data-ttu-id="6b894-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b894-135">RELATED LINKS</span></span>

[<span data-ttu-id="6b894-136">Új – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6b894-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="6b894-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6b894-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="6b894-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6b894-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


