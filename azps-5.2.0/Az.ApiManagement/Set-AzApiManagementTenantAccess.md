---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361841"
---
# <span data-ttu-id="1b3e2-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1b3e2-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="1b3e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3e2-103">Engedélyezi vagy letiltja a bérlő hozzáférését.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="1b3e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b3e2-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b3e2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b3e2-105">DESCRIPTION</span></span>
<span data-ttu-id="1b3e2-106">A **Set-AzApiManagementTenantAccess** parancsmag engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="1b3e2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b3e2-107">EXAMPLES</span></span>

### <span data-ttu-id="1b3e2-108">1. példa: Bérlői hozzáférés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="1b3e2-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="1b3e2-109">Ez a parancs lehetővé teszi a bérlő hozzáférését a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="1b3e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b3e2-110">PARAMETERS</span></span>

### <span data-ttu-id="1b3e2-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1b3e2-111">-Context</span></span>
<span data-ttu-id="1b3e2-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b3e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3e2-113">-DefaultProfile</span></span>
<span data-ttu-id="1b3e2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b3e2-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="1b3e2-115">-Enabled</span></span>
<span data-ttu-id="1b3e2-116">Azt adja meg, hogy ez a parancsmag engedélyezi vagy letiltja-e a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="1b3e2-117">Adja meg a letiltani $True vagy letiltani $False értéket.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3e2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3e2-118">-PassThru</span></span>
<span data-ttu-id="1b3e2-119">Azt jelzi, hogy ez a parancsmag a **psApiManagementAccessInformation** értéket adja vissza, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1b3e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3e2-120">CommonParameters</span></span>
<span data-ttu-id="1b3e2-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3e2-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b3e2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3e2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b3e2-123">INPUTS</span></span>

### <span data-ttu-id="1b3e2-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b3e2-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1b3e2-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b3e2-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b3e2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b3e2-126">OUTPUTS</span></span>

### <span data-ttu-id="1b3e2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1b3e2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1b3e2-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b3e2-128">NOTES</span></span>

## <span data-ttu-id="1b3e2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b3e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="1b3e2-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1b3e2-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


