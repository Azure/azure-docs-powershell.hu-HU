---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478893"
---
# <span data-ttu-id="7ccb3-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="7ccb3-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="7ccb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ccb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccb3-103">Egy bérlő Git-hozzáférési konfigurációs kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="7ccb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ccb3-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ccb3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ccb3-105">DESCRIPTION</span></span>
<span data-ttu-id="7ccb3-106">Egy bérlő Git-hozzáférési konfigurációs kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="7ccb3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ccb3-107">EXAMPLES</span></span>

### <span data-ttu-id="7ccb3-108">1. példa: Bérlői hozzáférés beállítása</span><span class="sxs-lookup"><span data-stu-id="7ccb3-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="7ccb3-109">Ez a parancs a Git-hozzáférés konfigurációs kulcsait kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="7ccb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ccb3-110">PARAMETERS</span></span>

### <span data-ttu-id="7ccb3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7ccb3-111">-Context</span></span>
<span data-ttu-id="7ccb3-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7ccb3-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7ccb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccb3-114">-DefaultProfile</span></span>
<span data-ttu-id="7ccb3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccb3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccb3-116">CommonParameters</span></span>
<span data-ttu-id="7ccb3-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ccb3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccb3-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ccb3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccb3-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ccb3-119">INPUTS</span></span>

### <span data-ttu-id="7ccb3-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ccb3-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="7ccb3-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ccb3-121">OUTPUTS</span></span>

### <span data-ttu-id="7ccb3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="7ccb3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7ccb3-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ccb3-123">NOTES</span></span>

## <span data-ttu-id="7ccb3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ccb3-124">RELATED LINKS</span></span>
