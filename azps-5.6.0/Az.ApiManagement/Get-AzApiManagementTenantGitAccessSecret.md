---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004870"
---
# <span data-ttu-id="da9c8-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="da9c8-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="da9c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="da9c8-103">Egy bérlő Git-hozzáférési konfigurációs kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da9c8-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="da9c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da9c8-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9c8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da9c8-105">DESCRIPTION</span></span>
<span data-ttu-id="da9c8-106">Egy bérlő Git-hozzáférési konfigurációs kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da9c8-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="da9c8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da9c8-107">EXAMPLES</span></span>

### <span data-ttu-id="da9c8-108">1. példa: Bérlői hozzáférés beállítása</span><span class="sxs-lookup"><span data-stu-id="da9c8-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="da9c8-109">Ez a parancs a Git-hozzáférés konfigurációs kulcsait kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="da9c8-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="da9c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da9c8-110">PARAMETERS</span></span>

### <span data-ttu-id="da9c8-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="da9c8-111">-Context</span></span>
<span data-ttu-id="da9c8-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="da9c8-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da9c8-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="da9c8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="da9c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9c8-114">-DefaultProfile</span></span>
<span data-ttu-id="da9c8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da9c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da9c8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9c8-116">CommonParameters</span></span>
<span data-ttu-id="da9c8-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9c8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9c8-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da9c8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9c8-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da9c8-119">INPUTS</span></span>

### <span data-ttu-id="da9c8-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da9c8-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="da9c8-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9c8-121">OUTPUTS</span></span>

### <span data-ttu-id="da9c8-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="da9c8-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="da9c8-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da9c8-123">NOTES</span></span>

## <span data-ttu-id="da9c8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da9c8-124">RELATED LINKS</span></span>
