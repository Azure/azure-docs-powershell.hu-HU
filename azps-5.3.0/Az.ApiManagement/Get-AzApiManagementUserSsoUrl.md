---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478882"
---
# <span data-ttu-id="5e92f-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="5e92f-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="5e92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e92f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e92f-103">Egy felhasználó SSO URL-címét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5e92f-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="5e92f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e92f-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e92f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e92f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e92f-106">A **Get-AzApiManagementUserSsoUrl** parancsmag egyetlen bejelentkezési URL-címet hoz létre a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="5e92f-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="5e92f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e92f-107">EXAMPLES</span></span>

### <span data-ttu-id="5e92f-108">1. példa: Felhasználó SSO URL-címének lekérte</span><span class="sxs-lookup"><span data-stu-id="5e92f-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5e92f-109">Ez a parancs a felhasználó SSO URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="5e92f-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="5e92f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e92f-110">PARAMETERS</span></span>

### <span data-ttu-id="5e92f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5e92f-111">-Context</span></span>
<span data-ttu-id="5e92f-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="5e92f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5e92f-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5e92f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5e92f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e92f-114">-DefaultProfile</span></span>
<span data-ttu-id="5e92f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e92f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e92f-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="5e92f-116">-UserId</span></span>
<span data-ttu-id="5e92f-117">Felhasználóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5e92f-117">Specifies a user ID.</span></span>
<span data-ttu-id="5e92f-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5e92f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5e92f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e92f-119">CommonParameters</span></span>
<span data-ttu-id="5e92f-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e92f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e92f-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e92f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e92f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e92f-122">INPUTS</span></span>

### <span data-ttu-id="5e92f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5e92f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e92f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5e92f-124">System.String</span></span>

## <span data-ttu-id="5e92f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e92f-125">OUTPUTS</span></span>

### <span data-ttu-id="5e92f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5e92f-126">System.String</span></span>

## <span data-ttu-id="5e92f-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e92f-127">NOTES</span></span>

## <span data-ttu-id="5e92f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e92f-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e92f-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5e92f-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


