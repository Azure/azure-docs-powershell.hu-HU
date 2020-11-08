---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182820"
---
# <span data-ttu-id="fbbb9-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fbbb9-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="fbbb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbbb9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb9-103">Törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fbbb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbbb9-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbbb9-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbb9-106">A **Remove-AzDataLakeStoreItemAcl** parancsmag törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fbbb9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbbb9-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbb9-108">1. példa: az ACL eltávolítása mappából</span><span class="sxs-lookup"><span data-stu-id="fbbb9-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="fbbb9-109">Ez a parancs eltávolítja az ContosoADL-fiók gyökérkönyvtárának hozzáférés-vezérlési mappáját.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="fbbb9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbbb9-110">PARAMETERS</span></span>

### <span data-ttu-id="fbbb9-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fbbb9-111">-Account</span></span>
<span data-ttu-id="fbbb9-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-113">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fbbb9-113">-Default</span></span>
<span data-ttu-id="fbbb9-114">Azt jelzi, hogy a parancsmag eltávolítja egy fájl vagy mappa alapértelmezett hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb9-115">-DefaultProfile</span></span>
<span data-ttu-id="fbbb9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbbb9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fbbb9-117">-Force</span></span>
<span data-ttu-id="fbbb9-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbbb9-119">-PassThru</span></span>
<span data-ttu-id="fbbb9-120">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="fbbb9-121">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fbbb9-121">-Path</span></span>
<span data-ttu-id="fbbb9-122">Az elem az adattó-tároló elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="fbbb9-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbbb9-123">-Confirm</span></span>
<span data-ttu-id="fbbb9-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbb9-125">-WhatIf</span></span>
<span data-ttu-id="fbbb9-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbb9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb9-128">CommonParameters</span></span>
<span data-ttu-id="fbbb9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbbb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb9-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbb9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbbb9-131">INPUTS</span></span>

### <span data-ttu-id="fbbb9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fbbb9-132">System.String</span></span>

### <span data-ttu-id="fbbb9-133">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fbbb9-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fbbb9-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fbbb9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbbb9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbbb9-135">OUTPUTS</span></span>

### <span data-ttu-id="fbbb9-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbbb9-136">System.Boolean</span></span>

## <span data-ttu-id="fbbb9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-137">NOTES</span></span>
* <span data-ttu-id="fbbb9-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="fbbb9-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="fbbb9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbbb9-139">RELATED LINKS</span></span>

[<span data-ttu-id="fbbb9-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fbbb9-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="fbbb9-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fbbb9-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="fbbb9-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fbbb9-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


