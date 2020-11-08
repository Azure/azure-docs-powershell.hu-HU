---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187859"
---
# <span data-ttu-id="b2c92-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b2c92-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="b2c92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2c92-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c92-103">Engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="b2c92-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="b2c92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2c92-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2c92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2c92-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c92-106">A **set-AzApiManagementTenantAccess** parancsmag engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="b2c92-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="b2c92-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b2c92-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c92-108">1. példa: a bérlői hozzáférés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="b2c92-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="b2c92-109">Ez a parancs engedélyezi a bérlői hozzáférést a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="b2c92-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="b2c92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2c92-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c92-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b2c92-111">-Context</span></span>
<span data-ttu-id="b2c92-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2c92-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b2c92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c92-113">-DefaultProfile</span></span>
<span data-ttu-id="b2c92-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2c92-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2c92-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b2c92-115">-Enabled</span></span>
<span data-ttu-id="b2c92-116">Megadja, hogy ez a parancsmag engedélyezi vagy tiltja-e a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="b2c92-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="b2c92-117">Adja meg a letiltáshoz vagy az $False engedélyezéséhez $True értékét.</span><span class="sxs-lookup"><span data-stu-id="b2c92-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="b2c92-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2c92-118">-PassThru</span></span>
<span data-ttu-id="b2c92-119">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementAccessInformation** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b2c92-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b2c92-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c92-120">CommonParameters</span></span>
<span data-ttu-id="b2c92-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2c92-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c92-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2c92-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c92-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c92-123">INPUTS</span></span>

### <span data-ttu-id="b2c92-124">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2c92-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b2c92-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b2c92-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b2c92-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c92-126">OUTPUTS</span></span>

### <span data-ttu-id="b2c92-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b2c92-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b2c92-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2c92-128">NOTES</span></span>

## <span data-ttu-id="b2c92-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2c92-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2c92-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b2c92-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


