---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672284"
---
# <span data-ttu-id="277e1-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="277e1-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="277e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="277e1-102">SYNOPSIS</span></span>
<span data-ttu-id="277e1-103">Egy API-kezelési tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="277e1-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="277e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="277e1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="277e1-105">DESCRIPTION</span></span>
<span data-ttu-id="277e1-106">A **Remove-AzureRmApiManagementCertificate** parancsmag eltávolítja az Azure API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="277e1-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="277e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="277e1-107">EXAMPLES</span></span>

### <span data-ttu-id="277e1-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="277e1-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="277e1-109">Ez a parancs eltávolítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="277e1-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="277e1-110">Mivel az *erő* paraméter van megadva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="277e1-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="277e1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="277e1-111">PARAMETERS</span></span>

### <span data-ttu-id="277e1-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="277e1-112">-CertificateId</span></span>
<span data-ttu-id="277e1-113">Az eltávolítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="277e1-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277e1-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="277e1-114">-Context</span></span>
<span data-ttu-id="277e1-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="277e1-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277e1-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="277e1-116">-PassThru</span></span>
<span data-ttu-id="277e1-117">passthru</span><span class="sxs-lookup"><span data-stu-id="277e1-117">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277e1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="277e1-118">-Confirm</span></span>
<span data-ttu-id="277e1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="277e1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277e1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277e1-120">-WhatIf</span></span>
<span data-ttu-id="277e1-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="277e1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277e1-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="277e1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277e1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277e1-123">-DefaultProfile</span></span>
<span data-ttu-id="277e1-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="277e1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277e1-125">CommonParameters</span></span>
<span data-ttu-id="277e1-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="277e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277e1-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277e1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277e1-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="277e1-128">INPUTS</span></span>

## <span data-ttu-id="277e1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="277e1-129">OUTPUTS</span></span>

### <span data-ttu-id="277e1-130">Logikai</span><span class="sxs-lookup"><span data-stu-id="277e1-130">Boolean</span></span>

## <span data-ttu-id="277e1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="277e1-131">NOTES</span></span>

## <span data-ttu-id="277e1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="277e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="277e1-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="277e1-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="277e1-134">Új – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="277e1-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="277e1-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="277e1-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


