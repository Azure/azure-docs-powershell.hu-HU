---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154523"
---
# <span data-ttu-id="b8722-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="b8722-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="b8722-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8722-102">SYNOPSIS</span></span>
<span data-ttu-id="b8722-103">Részleteket kap az Azure NetApp-fájlok (ANF) Active Directory-konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="b8722-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="b8722-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8722-104">SYNTAX</span></span>

### <span data-ttu-id="b8722-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8722-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8722-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8722-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8722-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8722-107">DESCRIPTION</span></span>
<span data-ttu-id="b8722-108">A **Get-AzNetAppFilesActiveDirectory** parancsmag az ANF-fiókok Active Directory-konfigurációjának részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b8722-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="b8722-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8722-109">EXAMPLES</span></span>

### <span data-ttu-id="b8722-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b8722-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="b8722-111">Ez a parancs a MyAnfAccount nevű Azure NetApp-fájlok (ANF) fiók MyADConfigName nevű AD-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8722-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="b8722-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8722-112">PARAMETERS</span></span>

### <span data-ttu-id="b8722-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b8722-113">-AccountName</span></span>
<span data-ttu-id="b8722-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b8722-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b8722-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b8722-115">-AccountObject</span></span>
<span data-ttu-id="b8722-116">Az új Active Directory-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="b8722-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8722-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="b8722-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="b8722-118">The ActiveDirectoryId of the ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="b8722-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8722-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8722-119">-DefaultProfile</span></span>
<span data-ttu-id="b8722-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8722-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8722-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8722-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8722-122">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="b8722-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b8722-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8722-123">CommonParameters</span></span>
<span data-ttu-id="b8722-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8722-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8722-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8722-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8722-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8722-126">INPUTS</span></span>

### <span data-ttu-id="b8722-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b8722-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b8722-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8722-128">OUTPUTS</span></span>

### <span data-ttu-id="b8722-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="b8722-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="b8722-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8722-130">NOTES</span></span>

## <span data-ttu-id="b8722-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8722-131">RELATED LINKS</span></span>
