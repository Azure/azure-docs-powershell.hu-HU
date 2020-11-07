---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844358"
---
# <span data-ttu-id="40686-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="40686-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="40686-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40686-102">SYNOPSIS</span></span>
<span data-ttu-id="40686-103">SQL Server-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="40686-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="40686-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40686-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40686-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40686-105">DESCRIPTION</span></span>
<span data-ttu-id="40686-106">A **Remove-AzVMSqlServerExtension** parancsmag eltávolítja a AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="40686-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="40686-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40686-107">EXAMPLES</span></span>

### <span data-ttu-id="40686-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="40686-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="40686-109">Ez a parancs eltávolítja az SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="40686-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="40686-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40686-110">PARAMETERS</span></span>

### <span data-ttu-id="40686-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40686-111">-DefaultProfile</span></span>
<span data-ttu-id="40686-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40686-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40686-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40686-113">-Name</span></span>
<span data-ttu-id="40686-114">Annak az SQL-kiszolgálónak a neve, amely a parancsmag által eltávolított bővítmény.</span><span class="sxs-lookup"><span data-stu-id="40686-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40686-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40686-115">-ResourceGroupName</span></span>
<span data-ttu-id="40686-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40686-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40686-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="40686-117">-VMName</span></span>
<span data-ttu-id="40686-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="40686-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40686-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40686-119">CommonParameters</span></span>
<span data-ttu-id="40686-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40686-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40686-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40686-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40686-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40686-122">INPUTS</span></span>

### <span data-ttu-id="40686-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="40686-123">None</span></span>
<span data-ttu-id="40686-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="40686-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40686-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40686-125">OUTPUTS</span></span>

### <span data-ttu-id="40686-126">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="40686-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="40686-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40686-127">NOTES</span></span>

## <span data-ttu-id="40686-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40686-128">RELATED LINKS</span></span>

[<span data-ttu-id="40686-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="40686-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="40686-130">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="40686-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


