---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: fc22515fc1d1fc4c3975ee315ec9f7bf611e67c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667986"
---
# <span data-ttu-id="25091-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="25091-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="25091-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25091-102">SYNOPSIS</span></span>
<span data-ttu-id="25091-103">Egy API-kezelési tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="25091-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="25091-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25091-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25091-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25091-105">DESCRIPTION</span></span>
<span data-ttu-id="25091-106">A **Remove-AzApiManagementCertificate** parancsmag eltávolítja az Azure API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="25091-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="25091-107">Példák</span><span class="sxs-lookup"><span data-stu-id="25091-107">EXAMPLES</span></span>

### <span data-ttu-id="25091-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="25091-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="25091-109">Ez a parancs eltávolítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="25091-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="25091-110">Mivel az *erő* paraméter van megadva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="25091-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="25091-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25091-111">PARAMETERS</span></span>

### <span data-ttu-id="25091-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="25091-112">-CertificateId</span></span>
<span data-ttu-id="25091-113">Az eltávolítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25091-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="25091-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="25091-114">-Context</span></span>
<span data-ttu-id="25091-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="25091-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25091-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25091-116">-DefaultProfile</span></span>
<span data-ttu-id="25091-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25091-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25091-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25091-118">-PassThru</span></span>
<span data-ttu-id="25091-119">passthru</span><span class="sxs-lookup"><span data-stu-id="25091-119">passthru</span></span>

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

### <span data-ttu-id="25091-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25091-120">-Confirm</span></span>
<span data-ttu-id="25091-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25091-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25091-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25091-122">-WhatIf</span></span>
<span data-ttu-id="25091-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25091-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25091-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25091-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25091-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25091-125">CommonParameters</span></span>
<span data-ttu-id="25091-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25091-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25091-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25091-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25091-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25091-128">INPUTS</span></span>

### <span data-ttu-id="25091-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25091-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25091-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25091-130">System.String</span></span>

### <span data-ttu-id="25091-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25091-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25091-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25091-132">OUTPUTS</span></span>

### <span data-ttu-id="25091-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25091-133">System.Boolean</span></span>

## <span data-ttu-id="25091-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25091-134">NOTES</span></span>

## <span data-ttu-id="25091-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25091-135">RELATED LINKS</span></span>

[<span data-ttu-id="25091-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="25091-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="25091-137">Új – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="25091-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="25091-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="25091-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


