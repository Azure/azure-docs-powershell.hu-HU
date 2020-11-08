---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185590"
---
# <span data-ttu-id="214e4-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="214e4-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="214e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="214e4-102">SYNOPSIS</span></span>
<span data-ttu-id="214e4-103">Jelentkezzen be egy Azure Container-nyilvántartóba.</span><span class="sxs-lookup"><span data-stu-id="214e4-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="214e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="214e4-104">SYNTAX</span></span>

### <span data-ttu-id="214e4-105">WithoutNameAndPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="214e4-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="214e4-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="214e4-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="214e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="214e4-107">DESCRIPTION</span></span>
<span data-ttu-id="214e4-108">Jelentkezzen be egy Azure Container-nyilvántartóba.</span><span class="sxs-lookup"><span data-stu-id="214e4-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="214e4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="214e4-109">EXAMPLES</span></span>

### <span data-ttu-id="214e4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="214e4-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="214e4-111">Jelentkezzen be az ACR-be hitelesítő adatokkal, ha már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="214e4-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="214e4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="214e4-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="214e4-113">Jelentkezzen be az ACR-be a rendszergazdai felhasználónevével és jelszavával, ha a rendszergazdai felhasználó engedélyezve volt.</span><span class="sxs-lookup"><span data-stu-id="214e4-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="214e4-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="214e4-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="214e4-115">Jelentkezzen be az ACR-be a Service Principal azonosítójával és jelszavával.</span><span class="sxs-lookup"><span data-stu-id="214e4-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="214e4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="214e4-116">PARAMETERS</span></span>

### <span data-ttu-id="214e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214e4-117">-DefaultProfile</span></span>
<span data-ttu-id="214e4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="214e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214e4-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="214e4-119">-Name</span></span>
<span data-ttu-id="214e4-120">Azure Container – rendszerleíró név.</span><span class="sxs-lookup"><span data-stu-id="214e4-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="214e4-121">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="214e4-121">-Password</span></span>
<span data-ttu-id="214e4-122">Az Azure Container beállításjegyzékének jelszava.</span><span class="sxs-lookup"><span data-stu-id="214e4-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214e4-123">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="214e4-123">-UserName</span></span>
<span data-ttu-id="214e4-124">Az Azure Container beállításjegyzékének felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="214e4-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214e4-125">CommonParameters</span></span>
<span data-ttu-id="214e4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="214e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214e4-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="214e4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214e4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="214e4-128">INPUTS</span></span>

### <span data-ttu-id="214e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="214e4-129">System.String</span></span>

## <span data-ttu-id="214e4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="214e4-130">OUTPUTS</span></span>

### <span data-ttu-id="214e4-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="214e4-131">System.Boolean</span></span>

## <span data-ttu-id="214e4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="214e4-132">NOTES</span></span>

## <span data-ttu-id="214e4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="214e4-133">RELATED LINKS</span></span>
