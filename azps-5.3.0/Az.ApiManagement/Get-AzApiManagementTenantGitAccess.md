---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478897"
---
# <span data-ttu-id="9eddf-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="9eddf-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="9eddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eddf-102">SYNOPSIS</span></span>
<span data-ttu-id="9eddf-103">Egy bérlő Git-hozzáférés-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eddf-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9eddf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9eddf-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9eddf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9eddf-105">DESCRIPTION</span></span>
<span data-ttu-id="9eddf-106">A **Get-AzApiManagementTenantGitAccess parancsmag** a Bérlő Git-hozzáférés-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eddf-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="9eddf-107">A billentyűk nem szerepelnek az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="9eddf-107">Keys will not be included into result details.</span></span> <span data-ttu-id="9eddf-108">Ha titkos ügyfélprogramot kap, használja a **Get-AzApiManagementTenantGitAccessSecret fájlt.**</span><span class="sxs-lookup"><span data-stu-id="9eddf-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="9eddf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9eddf-109">EXAMPLES</span></span>

### <span data-ttu-id="9eddf-110">1. példa: Bérlői hozzáférés beállítása</span><span class="sxs-lookup"><span data-stu-id="9eddf-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="9eddf-111">Ez a parancs a Git-hozzáférés konfigurációját kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="9eddf-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="9eddf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eddf-112">PARAMETERS</span></span>

### <span data-ttu-id="9eddf-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9eddf-113">-Context</span></span>
<span data-ttu-id="9eddf-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="9eddf-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9eddf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eddf-115">-DefaultProfile</span></span>
<span data-ttu-id="9eddf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eddf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eddf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eddf-117">CommonParameters</span></span>
<span data-ttu-id="9eddf-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eddf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eddf-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eddf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eddf-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9eddf-120">INPUTS</span></span>

### <span data-ttu-id="9eddf-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9eddf-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9eddf-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eddf-122">OUTPUTS</span></span>

### <span data-ttu-id="9eddf-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9eddf-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9eddf-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9eddf-124">NOTES</span></span>

## <span data-ttu-id="9eddf-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eddf-125">RELATED LINKS</span></span>
