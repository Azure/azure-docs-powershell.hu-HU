---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334385"
---
# <span data-ttu-id="a7944-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="a7944-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="a7944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7944-102">SYNOPSIS</span></span>
<span data-ttu-id="a7944-103">Állítsa be az adatokat egy sql virtuális gépcsoporthoz képest egy sql virtuális gép konfigurációjában.</span><span class="sxs-lookup"><span data-stu-id="a7944-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a7944-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7944-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7944-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7944-105">DESCRIPTION</span></span>
<span data-ttu-id="a7944-106">A Set-AzSqlVMConfigGroup parancsmag megszabadja az sql virtuális gép konfigurációjának sql virtuális gépcsoporthoz való csatlakozáshoz szükséges információkat.</span><span class="sxs-lookup"><span data-stu-id="a7944-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a7944-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7944-107">EXAMPLES</span></span>

### <span data-ttu-id="a7944-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a7944-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="a7944-109">Frissítse egy sql virtuális gép konfigurációjának csoportinformációit.</span><span class="sxs-lookup"><span data-stu-id="a7944-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a7944-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7944-110">PARAMETERS</span></span>

### <span data-ttu-id="a7944-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a7944-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="a7944-112">A fürtindító fiók jelszava</span><span class="sxs-lookup"><span data-stu-id="a7944-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="a7944-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a7944-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="a7944-114">A fürtszolgáltató-fiók jelszava</span><span class="sxs-lookup"><span data-stu-id="a7944-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="a7944-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7944-115">-DefaultProfile</span></span>
<span data-ttu-id="a7944-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7944-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7944-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a7944-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="a7944-118">Az SQL-szolgáltatásfiók jelszava</span><span class="sxs-lookup"><span data-stu-id="a7944-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="a7944-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="a7944-119">-SqlVM</span></span>
<span data-ttu-id="a7944-120">Az SQL virtuális gép konfigurációja, amelyhez csoporttagság lesz hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7944-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="a7944-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="a7944-121">-SqlVMGroup</span></span>
<span data-ttu-id="a7944-122">A csoport, amelybe az SQL virtuális gép fog</span><span class="sxs-lookup"><span data-stu-id="a7944-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="a7944-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7944-123">CommonParameters</span></span>
<span data-ttu-id="a7944-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7944-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7944-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7944-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7944-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7944-126">INPUTS</span></span>

### <span data-ttu-id="a7944-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a7944-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a7944-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7944-128">OUTPUTS</span></span>

### <span data-ttu-id="a7944-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a7944-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a7944-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7944-130">NOTES</span></span>

## <span data-ttu-id="a7944-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7944-131">RELATED LINKS</span></span>
