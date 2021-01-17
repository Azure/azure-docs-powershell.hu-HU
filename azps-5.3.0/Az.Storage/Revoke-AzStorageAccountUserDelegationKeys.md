---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466899"
---
# <span data-ttu-id="2e5b3-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="2e5b3-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="2e5b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5b3-103">Tárfiók felhasználói meghatalmazási kulcsának visszavonása</span><span class="sxs-lookup"><span data-stu-id="2e5b3-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="2e5b3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e5b3-104">SYNTAX</span></span>

### <span data-ttu-id="2e5b3-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e5b3-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5b3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2e5b3-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5b3-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2e5b3-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5b3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e5b3-108">DESCRIPTION</span></span>
<span data-ttu-id="2e5b3-109">A **Revoke-AzStorageAccountUserDelegationKeys** parancsmag visszavonja egy tárfiók összes felhasználói meghatalmazási kulcsát, így a tárfiók összes Identity SAS-jogkivonatát is visszavonja.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="2e5b3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e5b3-110">EXAMPLES</span></span>

### <span data-ttu-id="2e5b3-111">1. példa: Tárfiók felhasználói meghatalmazási kulcsának visszavonása</span><span class="sxs-lookup"><span data-stu-id="2e5b3-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="2e5b3-112">Ez a példa visszavonja egy tárfiók felhasználói meghatalmazási kulcsait, így a felhasználói meghatalmazási kulcsokból generált összes identity SAS-jogkivonat is vissza lesz vonva.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="2e5b3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e5b3-113">PARAMETERS</span></span>

### <span data-ttu-id="2e5b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5b3-114">-DefaultProfile</span></span>
<span data-ttu-id="2e5b3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5b3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e5b3-116">-InputObject</span></span>
<span data-ttu-id="2e5b3-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e5b3-118">-PassThru</span></span>
<span data-ttu-id="2e5b3-119">Ez a parancsmag általában nem ad vissza kimenetet a sikeres befejezéskor, ez a paraméter arra kényszeríti a parancsmagot, hogy sikeres befejezéskor értéket ($true) ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e5b3-121">A tárfiók-erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e5b3-122">-ResourceId</span></span>
<span data-ttu-id="2e5b3-123">Tárfiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2e5b3-124">-StorageAccountName</span></span>
<span data-ttu-id="2e5b3-125">A tárfiók-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e5b3-126">-Confirm</span></span>
<span data-ttu-id="2e5b3-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5b3-128">-WhatIf</span></span>
<span data-ttu-id="2e5b3-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5b3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5b3-131">CommonParameters</span></span>
<span data-ttu-id="2e5b3-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5b3-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5b3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5b3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e5b3-134">INPUTS</span></span>

### <span data-ttu-id="2e5b3-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e5b3-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2e5b3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e5b3-136">System.String</span></span>

## <span data-ttu-id="2e5b3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e5b3-137">OUTPUTS</span></span>

### <span data-ttu-id="2e5b3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e5b3-138">System.Boolean</span></span>

## <span data-ttu-id="2e5b3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e5b3-139">NOTES</span></span>

## <span data-ttu-id="2e5b3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e5b3-140">RELATED LINKS</span></span>
