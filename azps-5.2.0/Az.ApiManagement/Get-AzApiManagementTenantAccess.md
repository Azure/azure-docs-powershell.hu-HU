---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330989"
---
# <span data-ttu-id="bc2f7-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="bc2f7-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="bc2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2f7-103">A bérlői webhely hozzáférési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="bc2f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc2f7-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc2f7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2f7-106">A **Get-AzApiManagementTenantAccess** parancsmag beszerzi a bérlő hozzáférés-konfigurációját egy bérlőhöz.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="bc2f7-107">A billentyűk nem szerepelnek az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-107">Keys will not be included into result details.</span></span> <span data-ttu-id="bc2f7-108">Ha titkos ügyfélprogramot kap, használja a **Get-AzApiManagementTenantAccessSecret fájlt.**</span><span class="sxs-lookup"><span data-stu-id="bc2f7-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="bc2f7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc2f7-109">EXAMPLES</span></span>

### <span data-ttu-id="bc2f7-110">1. példa: Bérlői hozzáférés beállítása</span><span class="sxs-lookup"><span data-stu-id="bc2f7-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="bc2f7-111">Ez a parancs a bérlő hozzáférés-konfigurációját kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="bc2f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc2f7-112">PARAMETERS</span></span>

### <span data-ttu-id="bc2f7-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bc2f7-113">-Context</span></span>
<span data-ttu-id="bc2f7-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc2f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2f7-115">-DefaultProfile</span></span>
<span data-ttu-id="bc2f7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc2f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2f7-117">CommonParameters</span></span>
<span data-ttu-id="bc2f7-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc2f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2f7-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc2f7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2f7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc2f7-120">INPUTS</span></span>

### <span data-ttu-id="bc2f7-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc2f7-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bc2f7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc2f7-122">OUTPUTS</span></span>

### <span data-ttu-id="bc2f7-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="bc2f7-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="bc2f7-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc2f7-124">NOTES</span></span>

## <span data-ttu-id="bc2f7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc2f7-125">RELATED LINKS</span></span>

[<span data-ttu-id="bc2f7-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="bc2f7-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


