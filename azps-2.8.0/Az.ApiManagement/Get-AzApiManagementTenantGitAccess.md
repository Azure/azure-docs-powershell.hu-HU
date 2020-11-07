---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 3338ae75406cc7c9253b21a52726f283f19d4ad7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668086"
---
# <span data-ttu-id="9a71f-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="9a71f-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="9a71f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a71f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a71f-103">A git Access konfigurációját kapja egy bérlő számára.</span><span class="sxs-lookup"><span data-stu-id="9a71f-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9a71f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a71f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a71f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a71f-105">DESCRIPTION</span></span>
<span data-ttu-id="9a71f-106">A **Get-AzApiManagementTenantGitAccess** parancsmag a bérlői fiókhoz tartozó git Access-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="9a71f-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9a71f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a71f-107">EXAMPLES</span></span>

### <span data-ttu-id="9a71f-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="9a71f-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="9a71f-109">Ez a parancs a megadott környezetben a git Access konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9a71f-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="9a71f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a71f-110">PARAMETERS</span></span>

### <span data-ttu-id="9a71f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9a71f-111">-Context</span></span>
<span data-ttu-id="9a71f-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9a71f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9a71f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a71f-113">-DefaultProfile</span></span>
<span data-ttu-id="9a71f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a71f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a71f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a71f-115">CommonParameters</span></span>
<span data-ttu-id="9a71f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a71f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a71f-117">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9a71f-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a71f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a71f-118">INPUTS</span></span>

### <span data-ttu-id="9a71f-119">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a71f-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9a71f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a71f-120">OUTPUTS</span></span>

### <span data-ttu-id="9a71f-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9a71f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9a71f-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a71f-122">NOTES</span></span>

## <span data-ttu-id="9a71f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a71f-123">RELATED LINKS</span></span>
