---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467097"
---
# <span data-ttu-id="bbe26-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="bbe26-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="bbe26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe26-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe26-103">Állítsa be az adatokat egy sql virtuális gépcsoporthoz képest egy sql virtuális gép konfigurációjában.</span><span class="sxs-lookup"><span data-stu-id="bbe26-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bbe26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbe26-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbe26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbe26-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe26-106">A Set-AzSqlVMConfigGroup parancsmag megszabadja az sql virtuális gép konfigurációjának sql virtuális gépcsoporthoz való csatlakozáshoz szükséges információkat.</span><span class="sxs-lookup"><span data-stu-id="bbe26-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bbe26-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbe26-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe26-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bbe26-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="bbe26-109">Frissítse egy sql virtuális gép konfigurációjának csoportinformációit.</span><span class="sxs-lookup"><span data-stu-id="bbe26-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bbe26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbe26-110">PARAMETERS</span></span>

### <span data-ttu-id="bbe26-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bbe26-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="bbe26-112">A fürtindító fiók jelszava</span><span class="sxs-lookup"><span data-stu-id="bbe26-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe26-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bbe26-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="bbe26-114">A fürtszolgáltató-fiók jelszava</span><span class="sxs-lookup"><span data-stu-id="bbe26-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe26-115">-DefaultProfile</span></span>
<span data-ttu-id="bbe26-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbe26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe26-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bbe26-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="bbe26-118">Az SQL-szolgáltatásfiók jelszava</span><span class="sxs-lookup"><span data-stu-id="bbe26-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe26-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="bbe26-119">-SqlVM</span></span>
<span data-ttu-id="bbe26-120">Az SQL virtuális gép konfigurációja, amelyhez csoporttagság lesz hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bbe26-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe26-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="bbe26-121">-SqlVMGroup</span></span>
<span data-ttu-id="bbe26-122">A csoport, amelybe az SQL virtuális gép fog</span><span class="sxs-lookup"><span data-stu-id="bbe26-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe26-123">CommonParameters</span></span>
<span data-ttu-id="bbe26-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe26-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbe26-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe26-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbe26-126">INPUTS</span></span>

### <span data-ttu-id="bbe26-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="bbe26-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bbe26-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbe26-128">OUTPUTS</span></span>

### <span data-ttu-id="bbe26-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="bbe26-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bbe26-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbe26-130">NOTES</span></span>

## <span data-ttu-id="bbe26-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbe26-131">RELATED LINKS</span></span>
