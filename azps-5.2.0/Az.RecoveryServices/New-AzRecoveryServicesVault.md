---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355722"
---
# <span data-ttu-id="70d95-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70d95-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="70d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d95-102">SYNOPSIS</span></span>
<span data-ttu-id="70d95-103">Létrehoz egy új Helyreállítási szolgáltatások tárolót.</span><span class="sxs-lookup"><span data-stu-id="70d95-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="70d95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70d95-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d95-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70d95-105">DESCRIPTION</span></span>
<span data-ttu-id="70d95-106">A **New-AzRecoveryServicesVault** parancsmag létrehoz egy új Helyreállítási szolgáltatások tárolót.</span><span class="sxs-lookup"><span data-stu-id="70d95-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="70d95-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70d95-107">EXAMPLES</span></span>

### <span data-ttu-id="70d95-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="70d95-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="70d95-109">Helyreállítási szolgáltatás tároló létrehozása az erőforráscsoportban és a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="70d95-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="70d95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70d95-110">PARAMETERS</span></span>

### <span data-ttu-id="70d95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d95-111">-DefaultProfile</span></span>
<span data-ttu-id="70d95-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70d95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70d95-113">-Location</span><span class="sxs-lookup"><span data-stu-id="70d95-113">-Location</span></span>
<span data-ttu-id="70d95-114">A tároló földrajzi helyének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d95-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d95-115">-Name</span><span class="sxs-lookup"><span data-stu-id="70d95-115">-Name</span></span>
<span data-ttu-id="70d95-116">A létrehozni szükséges tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d95-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d95-117">-ResourceGroupName</span></span>
<span data-ttu-id="70d95-118">Annak az Azure-erőforráscsoportnak a nevét adja meg, amelyben létre kell hoznia vagy amelyből le kellkérni a megadott Recovery Services-objektumot.</span><span class="sxs-lookup"><span data-stu-id="70d95-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d95-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="70d95-119">-Tag</span></span>

<span data-ttu-id="70d95-120">Megadja a helyreállítási szolgáltatások tárolóhoz hozzáadni szükséges címkéket.</span><span class="sxs-lookup"><span data-stu-id="70d95-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d95-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70d95-121">-Confirm</span></span>
<span data-ttu-id="70d95-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70d95-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d95-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d95-123">-WhatIf</span></span>
<span data-ttu-id="70d95-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70d95-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70d95-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70d95-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d95-126">CommonParameters</span></span>
<span data-ttu-id="70d95-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d95-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70d95-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d95-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70d95-129">INPUTS</span></span>

### <span data-ttu-id="70d95-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="70d95-130">None</span></span>

## <span data-ttu-id="70d95-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70d95-131">OUTPUTS</span></span>

### <span data-ttu-id="70d95-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="70d95-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="70d95-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70d95-133">NOTES</span></span>

## <span data-ttu-id="70d95-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70d95-134">RELATED LINKS</span></span>

[<span data-ttu-id="70d95-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70d95-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="70d95-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="70d95-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="70d95-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70d95-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


