---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 7e07d6a23f88f869c75c9d2bcbb8b0270f92ebb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836960"
---
# <span data-ttu-id="b730d-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b730d-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="b730d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b730d-102">SYNOPSIS</span></span>
<span data-ttu-id="b730d-103">Egy API-kezelési tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b730d-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="b730d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b730d-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b730d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b730d-105">DESCRIPTION</span></span>
<span data-ttu-id="b730d-106">A **Remove-AzApiManagementCertificate** parancsmag eltávolítja az Azure API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b730d-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="b730d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b730d-107">EXAMPLES</span></span>

### <span data-ttu-id="b730d-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b730d-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="b730d-109">Ez a parancs eltávolítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b730d-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="b730d-110">Mivel az *erő* paraméter van megadva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="b730d-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="b730d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b730d-111">PARAMETERS</span></span>

### <span data-ttu-id="b730d-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b730d-112">-CertificateId</span></span>
<span data-ttu-id="b730d-113">Az eltávolítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b730d-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="b730d-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b730d-114">-Context</span></span>
<span data-ttu-id="b730d-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b730d-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b730d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b730d-116">-DefaultProfile</span></span>
<span data-ttu-id="b730d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b730d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b730d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b730d-118">-PassThru</span></span>
<span data-ttu-id="b730d-119">passthru</span><span class="sxs-lookup"><span data-stu-id="b730d-119">passthru</span></span>

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

### <span data-ttu-id="b730d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b730d-120">-Confirm</span></span>
<span data-ttu-id="b730d-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b730d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b730d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b730d-122">-WhatIf</span></span>
<span data-ttu-id="b730d-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b730d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b730d-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b730d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b730d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b730d-125">CommonParameters</span></span>
<span data-ttu-id="b730d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b730d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b730d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b730d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b730d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b730d-128">INPUTS</span></span>

### <span data-ttu-id="b730d-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b730d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b730d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b730d-130">System.String</span></span>

### <span data-ttu-id="b730d-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b730d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b730d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b730d-132">OUTPUTS</span></span>

### <span data-ttu-id="b730d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b730d-133">System.Boolean</span></span>

## <span data-ttu-id="b730d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b730d-134">NOTES</span></span>

## <span data-ttu-id="b730d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b730d-135">RELATED LINKS</span></span>

[<span data-ttu-id="b730d-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b730d-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="b730d-137">Új – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b730d-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="b730d-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b730d-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


