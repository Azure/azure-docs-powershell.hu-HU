---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185715"
---
# <span data-ttu-id="1e3ed-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1e3ed-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="1e3ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3ed-103">Azure NetApp-fájlok (ANF) fiókjának törlése</span><span class="sxs-lookup"><span data-stu-id="1e3ed-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="1e3ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e3ed-104">SYNTAX</span></span>

### <span data-ttu-id="1e3ed-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e3ed-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3ed-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e3ed-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3ed-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e3ed-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3ed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e3ed-108">DESCRIPTION</span></span>
<span data-ttu-id="1e3ed-109">A **Remove-AzNetAppFilesAccount** parancsmag törli az ANF-fiókját.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="1e3ed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e3ed-110">EXAMPLES</span></span>

### <span data-ttu-id="1e3ed-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e3ed-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="1e3ed-112">Ez a parancs törli a "MyAnfAccount" ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="1e3ed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e3ed-113">PARAMETERS</span></span>

### <span data-ttu-id="1e3ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3ed-114">-DefaultProfile</span></span>
<span data-ttu-id="1e3ed-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e3ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e3ed-116">-InputObject</span></span>
<span data-ttu-id="1e3ed-117">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="1e3ed-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ed-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e3ed-118">-Name</span></span>
<span data-ttu-id="1e3ed-119">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1e3ed-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ed-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e3ed-120">-PassThru</span></span>
<span data-ttu-id="1e3ed-121">A megadott fiók sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="1e3ed-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="1e3ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e3ed-123">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="1e3ed-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3ed-124">-ResourceId</span></span>
<span data-ttu-id="1e3ed-125">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1e3ed-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ed-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e3ed-126">-Confirm</span></span>
<span data-ttu-id="1e3ed-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3ed-128">-WhatIf</span></span>
<span data-ttu-id="1e3ed-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3ed-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3ed-131">CommonParameters</span></span>
<span data-ttu-id="1e3ed-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e3ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3ed-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e3ed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3ed-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e3ed-134">INPUTS</span></span>

### <span data-ttu-id="1e3ed-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3ed-135">System.String</span></span>

### <span data-ttu-id="1e3ed-136">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1e3ed-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1e3ed-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e3ed-137">OUTPUTS</span></span>

### <span data-ttu-id="1e3ed-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e3ed-138">System.Boolean</span></span>

## <span data-ttu-id="1e3ed-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e3ed-139">NOTES</span></span>

## <span data-ttu-id="1e3ed-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e3ed-140">RELATED LINKS</span></span>
