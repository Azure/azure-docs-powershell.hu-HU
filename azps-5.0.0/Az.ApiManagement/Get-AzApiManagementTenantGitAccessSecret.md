---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303875"
---
# <span data-ttu-id="11938-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="11938-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="11938-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11938-102">SYNOPSIS</span></span>
<span data-ttu-id="11938-103">A git hozzáférés konfigurációs kulcsait kapja bérlői fiókjában.</span><span class="sxs-lookup"><span data-stu-id="11938-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="11938-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11938-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11938-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11938-105">DESCRIPTION</span></span>
<span data-ttu-id="11938-106">A git hozzáférés konfigurációs kulcsait kapja bérlői fiókjában.</span><span class="sxs-lookup"><span data-stu-id="11938-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="11938-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11938-107">EXAMPLES</span></span>

### <span data-ttu-id="11938-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="11938-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="11938-109">Ez a parancs a git Access konfigurációs kulcsait kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="11938-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="11938-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11938-110">PARAMETERS</span></span>

### <span data-ttu-id="11938-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="11938-111">-Context</span></span>
<span data-ttu-id="11938-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="11938-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="11938-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="11938-113">This parameter is required.</span></span>

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

### <span data-ttu-id="11938-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11938-114">-DefaultProfile</span></span>
<span data-ttu-id="11938-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11938-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11938-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11938-116">CommonParameters</span></span>
<span data-ttu-id="11938-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11938-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11938-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11938-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11938-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11938-119">INPUTS</span></span>

### <span data-ttu-id="11938-120">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11938-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="11938-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11938-121">OUTPUTS</span></span>

### <span data-ttu-id="11938-122">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="11938-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="11938-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11938-123">NOTES</span></span>

## <span data-ttu-id="11938-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11938-124">RELATED LINKS</span></span>
