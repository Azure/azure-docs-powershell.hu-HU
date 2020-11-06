---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a70e3323bbd154005f014f1064a535f45a102f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492074"
---
# <span data-ttu-id="45eed-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45eed-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="45eed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45eed-102">SYNOPSIS</span></span>
<span data-ttu-id="45eed-103">Egy API-kezelési tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="45eed-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45eed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45eed-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45eed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45eed-105">DESCRIPTION</span></span>
<span data-ttu-id="45eed-106">A **Remove-AzureRmApiManagementCertificate** parancsmag eltávolítja az Azure API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="45eed-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="45eed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45eed-107">EXAMPLES</span></span>

### <span data-ttu-id="45eed-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="45eed-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="45eed-109">Ez a parancs eltávolítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="45eed-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="45eed-110">Mivel az *erő* paraméter van megadva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="45eed-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="45eed-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45eed-111">PARAMETERS</span></span>

### <span data-ttu-id="45eed-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="45eed-112">-CertificateId</span></span>
<span data-ttu-id="45eed-113">Az eltávolítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45eed-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="45eed-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="45eed-114">-Context</span></span>
<span data-ttu-id="45eed-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="45eed-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45eed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45eed-116">-DefaultProfile</span></span>
<span data-ttu-id="45eed-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45eed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45eed-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45eed-118">-PassThru</span></span>
<span data-ttu-id="45eed-119">passthru</span><span class="sxs-lookup"><span data-stu-id="45eed-119">passthru</span></span>

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

### <span data-ttu-id="45eed-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45eed-120">-Confirm</span></span>
<span data-ttu-id="45eed-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45eed-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45eed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45eed-122">-WhatIf</span></span>
<span data-ttu-id="45eed-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45eed-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45eed-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45eed-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45eed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45eed-125">CommonParameters</span></span>
<span data-ttu-id="45eed-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45eed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45eed-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45eed-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45eed-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45eed-128">INPUTS</span></span>

### <span data-ttu-id="45eed-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45eed-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45eed-130">System. String</span><span class="sxs-lookup"><span data-stu-id="45eed-130">System.String</span></span>

### <span data-ttu-id="45eed-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45eed-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45eed-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45eed-132">OUTPUTS</span></span>

### <span data-ttu-id="45eed-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45eed-133">System.Boolean</span></span>

## <span data-ttu-id="45eed-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45eed-134">NOTES</span></span>

## <span data-ttu-id="45eed-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45eed-135">RELATED LINKS</span></span>

[<span data-ttu-id="45eed-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45eed-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="45eed-137">Új – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45eed-137">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="45eed-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45eed-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


