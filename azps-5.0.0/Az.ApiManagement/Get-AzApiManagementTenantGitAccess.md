---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187946"
---
# <span data-ttu-id="67f76-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="67f76-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="67f76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67f76-102">SYNOPSIS</span></span>
<span data-ttu-id="67f76-103">A git Access konfigurációját kapja egy bérlő számára.</span><span class="sxs-lookup"><span data-stu-id="67f76-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="67f76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67f76-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67f76-105">DESCRIPTION</span></span>
<span data-ttu-id="67f76-106">A **Get-AzApiManagementTenantGitAccess** parancsmag a bérlői fiókhoz tartozó git Access-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="67f76-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="67f76-107">A billentyűk nem jelennek meg az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="67f76-107">Keys will not be included into result details.</span></span> <span data-ttu-id="67f76-108">Az ügyfél titkának beszerzéséhez használja a **Get-AzApiManagementTenantGitAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="67f76-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="67f76-109">Példák</span><span class="sxs-lookup"><span data-stu-id="67f76-109">EXAMPLES</span></span>

### <span data-ttu-id="67f76-110">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="67f76-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="67f76-111">Ez a parancs a megadott környezetben a git Access konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="67f76-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="67f76-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67f76-112">PARAMETERS</span></span>

### <span data-ttu-id="67f76-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="67f76-113">-Context</span></span>
<span data-ttu-id="67f76-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="67f76-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67f76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f76-115">-DefaultProfile</span></span>
<span data-ttu-id="67f76-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67f76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67f76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f76-117">CommonParameters</span></span>
<span data-ttu-id="67f76-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67f76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f76-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67f76-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f76-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f76-120">INPUTS</span></span>

### <span data-ttu-id="67f76-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="67f76-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="67f76-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f76-122">OUTPUTS</span></span>

### <span data-ttu-id="67f76-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="67f76-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="67f76-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67f76-124">NOTES</span></span>

## <span data-ttu-id="67f76-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f76-125">RELATED LINKS</span></span>
