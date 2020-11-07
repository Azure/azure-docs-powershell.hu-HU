---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836934"
---
# <span data-ttu-id="0b290-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0b290-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="0b290-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b290-102">SYNOPSIS</span></span>
<span data-ttu-id="0b290-103">Felhasználó eltávolítása egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="0b290-103">Removes a user from a group.</span></span>

## <span data-ttu-id="0b290-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b290-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b290-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b290-105">DESCRIPTION</span></span>
<span data-ttu-id="0b290-106">A **Remove-AzApiManagementUserFromGroup** parancsmag eltávolítja a felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="0b290-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="0b290-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0b290-107">EXAMPLES</span></span>

### <span data-ttu-id="0b290-108">1. példa: felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="0b290-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0b290-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="0b290-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="0b290-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b290-110">PARAMETERS</span></span>

### <span data-ttu-id="0b290-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0b290-111">-Context</span></span>
<span data-ttu-id="0b290-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0b290-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0b290-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0b290-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b290-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b290-114">-DefaultProfile</span></span>
<span data-ttu-id="0b290-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b290-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b290-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0b290-116">-GroupId</span></span>
<span data-ttu-id="0b290-117">Annak a csoportnak az AZONOSÍTÓját adja meg, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="0b290-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="0b290-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b290-118">-PassThru</span></span>
<span data-ttu-id="0b290-119">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="0b290-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0b290-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="0b290-120">-UserId</span></span>
<span data-ttu-id="0b290-121">Annak a felhasználónak az AZONOSÍTÓját adja meg, akit el szeretne távolítani a csoportból.</span><span class="sxs-lookup"><span data-stu-id="0b290-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="0b290-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b290-122">CommonParameters</span></span>
<span data-ttu-id="0b290-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b290-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b290-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b290-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b290-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b290-125">INPUTS</span></span>

### <span data-ttu-id="0b290-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0b290-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b290-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0b290-127">System.String</span></span>

### <span data-ttu-id="0b290-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0b290-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b290-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b290-129">OUTPUTS</span></span>

### <span data-ttu-id="0b290-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b290-130">System.Boolean</span></span>

## <span data-ttu-id="0b290-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b290-131">NOTES</span></span>

## <span data-ttu-id="0b290-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b290-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b290-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0b290-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="0b290-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0b290-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


