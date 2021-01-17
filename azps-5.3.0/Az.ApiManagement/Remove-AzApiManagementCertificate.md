---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382142"
---
# <span data-ttu-id="2e423-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2e423-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="2e423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e423-102">SYNOPSIS</span></span>
<span data-ttu-id="2e423-103">Eltávolít egy API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2e423-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="2e423-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e423-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e423-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e423-105">DESCRIPTION</span></span>
<span data-ttu-id="2e423-106">A **Remove-AzApiManagementCertificate** parancsmag eltávolítja az Azure API Management tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2e423-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="2e423-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e423-107">EXAMPLES</span></span>

### <span data-ttu-id="2e423-108">1. példa: Tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e423-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="2e423-109">Ez a parancs eltávolítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2e423-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="2e423-110">Mivel a *Force paraméter* meg van adva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="2e423-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="2e423-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e423-111">PARAMETERS</span></span>

### <span data-ttu-id="2e423-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2e423-112">-CertificateId</span></span>
<span data-ttu-id="2e423-113">Az eltávolítható tanúsítvány azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e423-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="2e423-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2e423-114">-Context</span></span>
<span data-ttu-id="2e423-115">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="2e423-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e423-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e423-116">-DefaultProfile</span></span>
<span data-ttu-id="2e423-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e423-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e423-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e423-118">-PassThru</span></span>
<span data-ttu-id="2e423-119">passthru</span><span class="sxs-lookup"><span data-stu-id="2e423-119">passthru</span></span>

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

### <span data-ttu-id="2e423-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e423-120">-Confirm</span></span>
<span data-ttu-id="2e423-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e423-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e423-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e423-122">-WhatIf</span></span>
<span data-ttu-id="2e423-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e423-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e423-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e423-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e423-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e423-125">CommonParameters</span></span>
<span data-ttu-id="2e423-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e423-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e423-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e423-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e423-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e423-128">INPUTS</span></span>

### <span data-ttu-id="2e423-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e423-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e423-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2e423-130">System.String</span></span>

### <span data-ttu-id="2e423-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e423-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e423-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e423-132">OUTPUTS</span></span>

### <span data-ttu-id="2e423-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e423-133">System.Boolean</span></span>

## <span data-ttu-id="2e423-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e423-134">NOTES</span></span>

## <span data-ttu-id="2e423-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e423-135">RELATED LINKS</span></span>

[<span data-ttu-id="2e423-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2e423-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="2e423-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2e423-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="2e423-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2e423-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


